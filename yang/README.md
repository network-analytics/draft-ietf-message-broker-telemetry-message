## YANG

```shell
$ pyang ietf-telemetry-message@2025-04-17.yang -f tree --tree-line-length 69 -p dependencies
$ pyang ietf-yang-push-telemetry-message@2025-04-17.yang -f tree --tree-line-length 69 -p dependencies
```

Full tree
```shell
$ pyang ietf-telemetry-message@2025-04-17.yang ietf-yang-push-telemetry-message@2025-04-17.yang -f tree --tree-line-length 69 -p deps
```

Format for Datatracker
```shell
$ pyang ietf-yang-push-telemetry-message@2025-04-17.yang -f yang --yang-line-length=69 -p deps
$ pyang ietf-telemetry-message@2025-04-17.yang -f yang --yang-line-length=69 -p deps
```
