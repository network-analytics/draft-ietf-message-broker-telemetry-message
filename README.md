IETF YANG Telemetry message draft.


# Validation
Examples are validated with `yanglint` version 4.2.2 tool from [libyang](https://github.com/CESNET/libyang)


Single Tree
```shell
$ yanglint ietf-telemetry-message@2025-10-19.yang -f tree --tree-line-length 69 -p deps
$ yanglint ietf-yang-push-telemetry-message@2025-10-19.yang -f tree --tree-line-length 69 -p deps
```

Full tree validating the schemas
```bash
yanglint -p yang/deps yang/ietf-yang-push-telemetry-message@2025-10-19.yang  yang/ietf-telemetry-message@2025-10-19.yang -f tree
```

Format for Datatracker
```shell
$ yanglint ietf-telemetry-message@2025-10-19.yang -f yang -p deps
$ yanglint ietf-yang-push-telemetry-message@2025-10-19.yang -f yang -p deps
```

Validating the example using YANG Library
```bash
yanglint -e -Y examples/lib.xml -p yang/deps -p yang  -t ext -k  ietf-telemetry-message:structure:message examples/example.json -f xml
```

Validating the example without using YANG Library
```bash
yanglint -t ext -k  ietf-telemetry-message:structure:message -p yang/deps  yang/deps/ietf-yang-push@2019-09-09.yang  yang/deps/ietf-udp-notif-transport@2025-02-14.yang  yang/deps/ietf-datastores@2018-02-14.yang  yang/ietf-yang-push-telemetry-message@2025-10-19.yang  yang/ietf-telemetry-message@2025-10-19.yang examples/example.json -f json
```

Validating the example telemetry-message with notification envelope payload using YANG Library (currently not working with yanglint 4.2.2)
```bash
yanglint -e -Y examples/lib.xml -p yang/deps -p yang  -t ext -k  ietf-telemetry-message:structure:message -k ietf-yp-notification:structure:envelope   examples/example-with-envelope.json -f json
YANGLINT[E]: Nothing to validate in the extension input data.
YANGLINT[E]: Failed to parse input data file "examples/example-with-envelope.json".
```

NOTE: validating just the envelope without the telemetry message works
```bash
yanglint -e -Y examples/lib.xml -p yang/deps -p yang  -t ext -k ietf-yp-notification:structure:envelope   examples/envelope.json -f json
```
