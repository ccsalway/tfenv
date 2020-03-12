# tfenv

**A way of setting the terraform version dynamically**

Written for zsh on macOS, although could easily be written for bash or other shells.

### Installation

1. Save the `terraform` file to a directory in your `$PATH`, for example, `/usr/local/bin`  
2. Make the file executable: `chmod +x /usr/local/bin/terraform`  

### Usage

Either:  

a) Create a file in your project called `.tf_version` which contains only the version of terraform you want to use  
```
% ls -la
-rw-r--r--   1 user  staff    6 Mar 12 07:19 .tf_version

% cat .tf_version
0.12.3

% terraform --version
Terraform v0.12.3
```

b) Set the environment variable `TFENV_VER`  
```
% TFENV_VER=0.11.0 terraform --version
Terraform v0.11.0
```

## Environment Variables

The following variables can be overridden with environment variables

`TFENV_URL` default: `https://releases.hashicorp.com`  
`TFENV_VER` default: contents of `.tf_version`  
`TFENV_ARCH` default: `darwin_amd64`  

For a list of releases and architectures, visit https://releases.hashicorp.com/terraform/
