[![release](https://github.com/Peters-IT/terraform-provider-hetzner-robot/actions/workflows/release.yml/badge.svg)](https://github.com/Peters-IT/terraform-provider-hetzner-robot/actions/workflows/release.yml)
# background to this fork

Initial found this via terraform (https://registry.terraform.io/providers/mwudka/hetznerrobot/latest) and here in github
at https://github.com/mwudka/terraform-provider-hetznerrobot, but it seems unfortunately it looks like it is no
longer maintained. As you can see, I have again made a fork of what I consider to be good improvements and new features
from https://github.com/SLoeuillet/terraform-provider-hetznerrobot.

I will try to keep this fork up to date, but this software comes without any guarantee of functionality. It is planned
to make a release available at terraform.

Feel free to submit merge/pull requests.

# features

- firewall
- vswitch
- ssh-key

# dependencies / tested with

- go 1.17.9
  - https://go.dev/dl/#go1.17.9
    - ``wget https://go.dev/dl/go1.17.9.linux-amd64.tar.gz``
    - ``rm -rf /usr/local/go && tar -C /usr/local -xzf go1.17.9.linux-amd64.tar.gz``
    - ``export PATH=$PATH:/usr/local/go/bin``
- terraform 1.1.8
  - https://www.terraform.io/downloads

# build
## local
```
goreleaser release --snapshot --skip-sign --rm-dist
```

## github
works with github action and goreleaser/action automatically at each new tag