## YANG

```shell
$ pyang ietf-telemetry-message@2025-04-12.yang -f tree --tree-line-length 69 -p dependencies
$ pyang ietf-yang-push-telemetry-message@2025-04-12.yang -f tree --tree-line-length 69 -p dependencies
```

Full tree
```shell
$ pyang ietf-telemetry-message@2025-04-12.yang ietf-yang-push-telemetry-message@2025-04-12.yang -f tree --tree-line-length 69 -p dependencies
```

Format for Datatracker
```shell
$ pyang ietf-yang-push-telemetry-message@2025-04-12.yang -f yang --yang-line-length=69 -p dependencies
$ pyang ietf-telemetry-message@2025-04-12.yang -f yang --yang-line-length=69 -p dependencies
```