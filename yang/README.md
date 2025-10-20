## YANG

```shell
$ yanglint ietf-telemetry-message@2025-10-19.yang -f tree --tree-line-length 69 -p deps
$ yanglint ietf-yang-push-telemetry-message@2025-10-19.yang -f tree --tree-line-length 69 -p deps
```

Full tree
```shell
$ yanglint ietf-telemetry-message@2025-10-19.yang ietf-yang-push-telemetry-message@2025-10-19.yang -f tree --tree-line-length 69 -p deps
```

Format for Datatracker
```shell
$ yanglint ietf-telemetry-message@2025-10-19.yang -f yang -p deps
$ yanglint ietf-yang-push-telemetry-message@2025-10-19.yang -f yang -p deps
```
