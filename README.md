IETF YANG Telemetry message draft.


# Validation

First change to the YANG dir.
```bash
cd yang
```

Validating the schemas
```bash
yanglint -p deps ietf-yang-push-telemetry-message@2024-02-20.yang  ietf-telemetry-message@2024-02-20.yang -f tree
```

Validating the example
```bash
yanglint -p deps --features=ietf-subscribed-notifications:xpath  ietf-yang-push-telemetry-message@2024-02-20.yang  ietf-telemetry-message@2024-02-20.yang ../examples/example.json
```
