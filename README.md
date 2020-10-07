# ansible-role-posh5


![Github Actions](https://img.shields.io/github/workflow/status/justin-p/ansible-role-posh5/CI?label=Github%20Actions&logo=github&style=flat-square)
![Travis](https://img.shields.io/travis/justin-p/ansible-role-posh5?label=Travis&logo=travis&style=flat-square)

This role will update PowerShell/Windows Management Framework to Version 5.1, enure that .Net applications use Strong TLS, configure NuGet, PowerShell Gallery, PowerShellGet and install the PSReadline Module.

All of this ensures that PowerShell functions like it does on modern Windows Systems. This ensures you can use `Install-Module` and by extend `win_psmodule` to install PowerShell modules or DSCs on older versions of Windows without any additional manual configuration.

Works on

- Windows Server 2019
- Windows Server 2016
- Windows Server 2012R2
- Windows Server 2012

Not validated (yet) on

- Windows Server 2008R2
- Windows Server 2008 x64
- Windows Server 2008 x32

## Requirements

N/A

## Role Variables

N/A

## Dependencies

N/A

## Example Playbook

    - hosts: posh5
      roles:
         - { role: justin_p.posh5 }

## Local Development

This role includes a Vagrantfile that will spin up a local Windows Server 2019 VM in Virtualbox.
After creating the VM it will automatically run our role.

### Development requirements

`pip3 install pywinrm`

#### Usage

- Run `vagrant up` to create a VM and run our playbook
- Run `vagrant provision` to reapply our playbook
- Run `vagrant destroy -f && vagrant up` to recreate the VM and run our playbook.
- Run `vagrant destroy` to remove the VM.

## License

MIT

## Authors

- Justin Perdok ([@justin-p](https://github.com/justin-p/)), Orange Cyberdefense
