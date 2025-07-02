IETF YANG Telemetry message draft.


# Validation

Validating the schemas (yanglint 3.7.8)
```bash
yanglint -p yang/deps yang/ietf-yang-push-telemetry-message@2025-06-10.yang  yang/ietf-telemetry-message@2025-06-10.yang -f tree
```

Validating the example using YANG Library (yanglint 3.7.8)
```bash
yanglint -e -Y examples/lib.json -p yang/deps examples/example.json -f json
```

Validating the example without using YANG Library  (yanglint 3.7.8)
```bash
yanglint -p yang/deps  yang/deps/ietf-yang-push@2019-09-09.yang  yang/deps/ietf-udp-notif-transport@2025-02-14.yang  yang/deps/ietf-datastores@2018-02-14.yang  yang/ietf-yang-push-telemetry-message@2025-06-10.yang  yang/ietf-telemetry-message@2025-06-10.yang examples/example.json -f json
```
