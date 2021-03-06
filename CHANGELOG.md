# perl Cookbook CHANGELOG

This file is used to list changes made in each version of the perl cookbook.

## 5.2.0 (2017-05-06)

- Fix license string to be a SPDX standard license string
- Simplify true/false statement
- Depend on a modern windows cookbook
- Require Chef 12.7+ to workaround an action_class bug

## 5.1.0 (2017-03-01)

- Resolve resource cloning in the test cookbook
- Test with Local Delivery instead of Rake
- Use the root_group attribute from Ohai instead of defining it ourselves
- Use multi-package to speed up installs in the default recipe
- Don’t use “module” as a resource property since its reserved. Instead use module_name and wire it up so a user can actually define a module name here instead of the module name coming from the name of the resource

## 5.0.0 (2017-02-27)

- Convert the existing HWRP to a custom resource and require Chef 12.5 and later

## 4.0.0 (2016-09-03)

- Testing updates
- Require Chef 12 or later

## v3.1.0 (2016-08-05)

- Added support for SUSE / openSUSE and IBM zlinux

## v3.0.0 (2016-04-07)

- Removed installation of the libwww-perl package, which is not required for Perl to function out of the box and can be installed by CPAN instead
- Resolved Chef 13 compatibility warnings in the cpan_module provider
- Updated the Windows Perl download URL to the new server
- Updated Perl to 5.22.1.3 on Windows
- Added the windows cookbook as a dependency so the Windows install converges
- Added module install / uninstall to the default Test Kitchen suite
- Added a basic Kitchen Inspec test to ensure perl is installed
- Added build-essential to the test cookbook so module installs would complete
- Added perl-devel to RHEL 6+ hosts

## v2.0.0 (2015-09-24)

- Rewrote cpan_module definition as a LWRP with Chefspec tests and matchers
- Add the ability to select version in the cpan_module LWRP
- Fixed cpan_module incompatibility with Chef 12
- Fixed download location for cpanm to prevent failures on the redirect
- Removed Chef 10 compatibility. This cookbook now requires 11+
- Added libwww-perl installation on Debian systems
- Added support for RHEL/CentOS 7 and Fedora to the default.rb recipe
- Added source_url and issues_url metadata
- Added a chefignore file to limit files uploaded to the server
- Updated Contributing and Testing docs
- Added a rakefile for simplified testing
- Added maintainers.md and maintainers.toml file and a Rake task for generating MD from TOML
- Updated platforms tested in Kitchen CI and update the Kitchen config format
- Updated to the standard chef .rubocop.yml file
- Updated all testing and development gems to the latest
- Add basic Chefspec test
- Updated Travis CI to test on modern ruby versions and reenabled rspec and foodcritic testing
- Added cookbook version and Travis CI badges to the readme
- Added a .foodcritic file to skip FC015
- Removed all references to Opscode
- Remove the Gemfile.lock that shouldn't have been committed

## v1.2.4 (2014-06-16)

- [COOK-4725] Use windows_path to set the PATH

## v1.2.2

### New Feature

- **[COOK-4013](https://tickets.chef.io/browse/COOK-4013)** - add omnios support to perl cookbook

## v1.2.0

### Improvement

- **[COOK-3230](https://tickets.chef.io/browse/COOK-3230)** - Upgrade cpanm
- **[COOK-2998](https://tickets.chef.io/browse/COOK-2998)** - Improve install speed by using `--notest`

## v1.1.2

### Bug

- [COOK-2973]: perl cookbook has foodcritic errors

## v1.1.0

- [COOK-1765] - Install Strawberry Perl on Windows in Perl Cookbook

## v1.0.2

- [COOK-1300] - add support for Mac OS X

## v1.0.0

- [COOK-1129] - move lists of perl packages to attributes by platform
- [COOK-1279] - resolve regression from COOK-1129
- [COOK-1299] - use App::cpanminus (cpanm) to install "cpan packages"

## v0.10.2

- [COOK-1279] Re-factor recipe and fix platform_version 5 bug for redhat family platforms

## v0.10.1

- [COOK-1129] centos/redhat needs the CPAN RPM installed

## v0.10.0

- Current released version
