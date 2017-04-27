﻿# puppet_vmwaretools

This vmwaretools ruby fact has been developped to be use in your puppet manifest.
Working for linux and windows operating system.


With this custom fact we can obtain : 

 - VMware tools is installed or not installed
 - VMware tools version
 - Where VMware tools has been installed (homedir)
 - Parameter timesync status (recommended to be disable if you have an ntp server configured)
 
 
 ---
 Example :
 
 For linux
 ```
#> facter -p vmwaretools
vmwaretools => {
  status => "installed",
  version => "10.0.5.52125 (build-3227872)",
  location => "/usr/bin/vmtoolsd",
  timesync => "disabled"
}
 ```
 
 For Windows
 ```
 #> facter -p vmwaretools
 vmwaretools => {
  status => "installed",
  location => "C:\Program Files\VMware\VMware Tools\",
  version => "10.1.6.4793 (build-5214329)",
  timesync => "disabled"
}
 ```
