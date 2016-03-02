# Crescendo Framework 2.0

Crescendo is the only free and open-source software framework for Crestron control systems. Crescendo is designed by [Adelyte Company](https://www.adelyte.com/) and maintained by the company and the community. Please visit the [project page](https://www.adelyte.com/crestron/crescendo) and [documentation](https://www.adelyte.com/crestron/crescendo/docs) for more information.

## Crescendo Cloud

The demo ships with the Crescendo Cloud driver embedded in a custom cloud controller. Data will be transmitted and saved to the Cloud from the moment the processor goes live. To see the data, add an email address to the `Users` parameter. Multiple email addresses can be separated by commas, the email address regular expression is rather resilient:

```coffeescript
/\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b/gi
```

If this functionality it not desired, simply comment out the `Z__Cloud_Connect` signal or the module entirely.

## Questions and Issues

Please submit a GitHub Issue for any question or issue.
