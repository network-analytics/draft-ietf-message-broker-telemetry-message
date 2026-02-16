IETF YANG Telemetry message draft.


# Validation
Examples are validated with development `yanglint` version 5.0.2 tool from [libyang](https://github.com/CESNET/libyang)


Single Tree
```shell
$ yanglint yang/ietf-telemetry-message@2025-10-19.yang -f tree --tree-line-length 69 -p yang/deps
$ yanglint yang/ietf-yang-push-telemetry-message@2025-10-19.yang -f tree --tree-line-length 69 -p dyang/deps
```

Full tree validating the schemas
```bash
yanglint -p yang/deps yang/ietf-yang-push-telemetry-message@2025-10-19.yang  yang/ietf-telemetry-message@2025-10-19.yang -f tree
```

Format for Datatracker
```shell
$ yanglint yang/ietf-telemetry-message@2025-10-19.yang -f yang -p yang/deps
$ yanglint yang/ietf-yang-push-telemetry-message@2025-10-19.yang -f yang -p yang/deps
```

Validating the example using YANG Library
```bash
yanglint -e -Y examples/lib.xml -p yang/deps -p yang examples/example.json -f xml
```

Validating the example without using YANG Library
```bash
yanglint --anydata-strict -p yang/deps yang/deps/ietf-yang-push@2019-09-09.yang yang/deps/ietf-udp-notif-transport@2025-02-14.yang yang/deps/ietf-datastores@2018-02-14.yang yang/ietf-yang-push-telemetry-message@2025-10-19.yang yang/ietf-telemetry-message@2025-10-19.yang examples/example.json -f json
```

Validating the example telemetry-message with notification envelope payload using YANG Library (currently working with yanglint 5.0.4)
```bash
yanglint --anydata-strict -e -Y examples/lib.xml -p yang/deps -p yang examples/example-with-envelope.json -f json
```

NOTE: validating just the envelope without the telemetry message works
```bash
yanglint -e -Y examples/lib.xml -p yang/deps -p yang   examples/envelope.json -f json
```
