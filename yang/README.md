## YANG

```shell
$ pyang ietf-telemetry-message@2025-10-19.yang -f tree --tree-line-length 69 -p deps
$ pyang ietf-yang-push-telemetry-message@2025-08-15.yang -f tree --tree-line-length 69 -p deps
```

Full tree
```shell
$ pyang ietf-telemetry-message@2025-10-19.yang ietf-yang-push-telemetry-message@2025-08-15.yang -f tree --tree-line-length 69 -p deps
```

Format for Datatracker
```shell
$ pyang ietf-telemetry-message@2025-10-19.yang -f yang --yang-line-length=69 -p deps
$ pyang ietf-yang-push-telemetry-message@2025-08-15.yang -f yang --yang-line-length=69 -p deps
```
