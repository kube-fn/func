# Functions

```yaml
kind: Function
metadata:
  name: contact-form-submission
spec:
  image: example/submit-form
  maxReplicas: 10
  persistance:
    gracePeriod: 10s
  triggers:
  - http-contact-form-submit
```