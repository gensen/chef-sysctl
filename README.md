# DESCRIPTION:
Set sysctl values from Chef!

This is a fork of the sysctl cookbook from [avishai](http://community.opscode.com/cookbooks/sysctl) combined with the work of [damm](https://github.com/damm/sysctl) for ease of use.

# REQUIREMENTS:

# ATTRIBUTES:
node[:sysctl] = A namespace for sysctl settings.

# USAGE:
There are ~~two~~ *three* ways of setting sysctl values:

1. Set chef attributes in the _sysctl_ namespace, E.G.:

    default[:sysctl][:vm][:swappiness] = 20</tt>

2. Set values in a cookbook_file - 69-chef-static.conf
3. Using the `sysctl` definition inside a cookbook

    sysctl "What am I doing" do
      variables 'kernel.sem' => node[:blah][:kernel_sem]
    end
