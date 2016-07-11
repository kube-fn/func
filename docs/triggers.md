# Triggers

Triggers receive messages from various sources, and create func messages that cause can consequently cause functions to run.

Example triggers can be messages on a Redis queue, RabbitMQ, or an HTTP request. Ultimately they receive data and transmit
it back to the controller to be handled.

```yaml
kind: Trigger
metadata:
  name: http-contact-form-submit
spec:
  image: kube-fn/trigger-http
  config: -|
    url: example.com/submit
    type: POST # could be *
    ingress: true # create ingress resource for this trigger
```