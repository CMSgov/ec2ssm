### Requirements

- vpn access
- configured AWS CLI
- [AWS Session Manager plugin for AWS CLI](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html), can be verified with the command: `session-manager-plugin`
- [go installed](https://go.dev/doc/install), make sure to have ~/go/bin in your path

# Installation
## Method 1 (download prebuild)
```
go install github.com/oddballteam/ec2ssm@latest
```

## Method 2 (build locally)
```
git clone https://github.com/CMSgov/ec2ssm.git
cd ec2ssm
go install
```

## Method 3 (download prebuild without Go)
Go to the [release page](https://github.com/oddballteam/ec2ssm/releases). Unzip the archive and add the ec2ssm binary to a folder already in your path.

# Usage
```
ec2ssm
```

run `ec2ssm` and select the instance you would like to connect to using the arrow keys.

### Issues
This is a new tool and likely will have issues. 
You can message `@Doug Moore` if you run into an issue.
There is no validity checking on if a session CAN be made. 
So, before submitting first attempt to make a ssm session without `ec2ssm`

This can be attempted with `aws ssm start-session --target i-INSTANCE_ID_HERE`

### Build
Builds are can be done locally but prebuilds can also be built out as outlined [here](https://github.com/oddballteam/ec2ssm#build)
