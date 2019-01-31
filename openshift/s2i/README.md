# s2i Images Reference
-[devtools/go-toolset-1.10-rhel7](https://access.redhat.com/containers/?architecture=AMD64&tab=docker-file#/registry.access.redhat.com/devtools/go-toolset-1.10-rhel7/images/1.10.3-15) Size 272.3 MB

- [rhscl/s2i-base-rhel7](https://access.redhat.com/containers/?architecture=AMD64&tab=docker-file#/registry.access.redhat.com/rhscl/s2i-base-rhel7/images/1-63) Size 161.1MB


- [rhscl/s2i-core-rhel7](https://access.redhat.com/containers/?architecture=AMD64&tab=docker-file#/registry.access.redhat.com/rhscl/s2i-core-rhel7/images/1-47) Size 78.7MB

# Import-Images

- oc import-image go-toolset-1.10-rhel7:1.10.3-15 --from=registry.access.redhat.com/devtools/go-toolset-1.10-rhel7:1.10.3-15 --confirm

- oc import-image s2i-base-rhel7:1-63 --from=registry.access.redhat.com/rhscl/s2i-base-rhel7:1-63 --confirm

- oc import-image s2i-core-rhel7:1-47 --from=registry.access.redhat.com/rhscl/s2i-core-rhel7:1-47 --confirm 