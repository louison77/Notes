# Chef

## Principles

* Chef is a management configuration tool that works in mode client-server or autonomous.
* The autonomous mode use a command line `chef-solo`.
* Chef Infra takes charge of Linux, Windows, MacOS and Unix server configuration.
* Chef requires the installation of Chef-Workstation which included all the necesary tools to develop "cookbooks". These cookbooks are packages regrouping recipes configuring a specific component on target nodes.
* The recipes are written in ruby language.
* It easy to test chef recipes files with vagrant beacuse a chef plugin exists for vagrant.
* The actions are written in the files recipes/default.rb.

## Main commands

* `chef generate cookbook` : This command generates a cookbook folder from an empty directory.

## Good practices and tips

### Installation

```bash
wget https://packages.chef.io/files/stable/chef-workstation/21.10.640/ubuntu/20.04/chef-workstation_21.10.640-1_amd64.deb
sudo dpkg -i chef-workstation_21.10.640-1_amd64.deb
```

### Chef's recipe file example

```ruby
package 'code-server' do
  source "version_package"
  action :install
end
```
