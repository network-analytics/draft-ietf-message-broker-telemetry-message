IETF YANG Telemetry message draft.


# Validation

First change to the YANG dir.
```bash
cd yang
```

Validating the schemas (yanglint 3.7.8)
```bash
yanglint -p deps ietf-yang-push-telemetry-message@2025-04-17.yang  ietf-telemetry-message@2025-04-17.yang -f tree
```

Validating the example (yanglint 3.7.8)
```bash
yanglint -p deps deps/ietf-datastores@2018-02-14.yang deps/ietf-subscribed-notifications@2019-09-09.yang deps/ietf-udp-notif-transport@2025-02-14.yang ietf-yang-push-telemetry-message@2025-04-17.yang  ietf-telemetry-message@2025-04-17.yang  ../examples/example.json -f json
```
