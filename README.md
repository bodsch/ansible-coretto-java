# corretto java

ansible role for Amazon's Java implementation corretto.

- [corretto-8](https://docs.aws.amazon.com/corretto/latest/corretto-8-ug)
- [corretto-11](https://docs.aws.amazon.com/corretto/latest/corretto-11-ug)

default java version is 11

## tested operating systems

- CentOS 7 / 8
- Ubuntu 16 / 18
- Debian 9 / 10

## Supported Corretto Versions

- 8
- 11

## configuration parameters

```
java_version: 11

java_folder: /usr/lib/jvm
java_alias: "java-{{ java_version }}-corretto"

# https://github.com/corretto/corretto-8/releases
#  - https://docs.aws.amazon.com/corretto/latest/corretto-8-ug/downloads-list.html#download
# https://github.com/corretto/corretto-11/releases
#  - https://docs.aws.amazon.com/corretto/latest/corretto-11-ug/downloads-list.html#download

java_map:
  redhat:
    8: { url: "https://corretto.aws/downloads/resources/8.242.08.1/java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm", checksum: "md5:af146bc202ca2651381b286364ef45e2" }
    11: { url: "https://corretto.aws/downloads/resources/11.0.6.10.1/java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm", checksum: "md5:1e08469d0fbf8bd737171e4590721b1f" }

  debian:
    8: { url: "https://corretto.aws/downloads/resources/8.242.08.1/java-1.8.0-amazon-corretto-jdk_8.242.08-1_amd64.deb", checksum: "md5:3ece5f8ab9d68917e541e14c1fee6909" }
    11: { url: "https://corretto.aws/downloads/resources/11.0.6.10.1/java-11-amazon-corretto-jdk_11.0.6.10-1_amd64.deb", checksum: "md5:501e257d5389e26a024c01b47b4a8d80" }

  src:
    8: { url: "https://corretto.aws/downloads/resources/8.242.08.1/amazon-corretto-8.242.08.1-linux-x64.tar.gz", checksum: "md5:3a614a0e32aa5324843781d1077aad7a" }
    11: { url: "https://corretto.aws/downloads/resources/11.0.6.10.1/amazon-corretto-11.0.6.10.1-linux-x64.tar.gz", checksum: "md5:cfb0b142edf7ebc2f87a27405c8d39fc" }
```
