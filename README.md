<p align="center">
  <img src="logo\Total.png" alt="Total Productions"/>
</p>

# WinFCU
WinFCU is a rule based utility which keeps the file system clean by archiving/deleting/moving unwanted/unneeded files from the file system

WinFCU can be run interactivly, as a scheduled task or as a service

## Inno Setup

The WinFCU-x64 installer is created using "Inno Setup" v6.0.2

## Installing WinFCU

When installing WinFCU you have 3 options to choose from (Program Files are always installed. These are the WinFCU executable and require DLL Files);

- Configuration Files. These are the WinFCU.exe.config and the log4net.config
  Exclude these from installing when you are upgrading WinFCU (aka prevent loosing your current setup)
  Possible required changes to these files will be documented in the release notes
- Example Files. 3 example files can be installed in the WinFCU include folder. These files form a solid base of
  cleaning up the Temp, Windows and Users folders on the system drive
- Install WinFCU as service. This will do as it says......

### Commandline options

```
  .\WinFCU-x64-<version>.exe                          Installs everything and installs WinFCU as service
  .\WinFCU-x64-<version>.exe /COMPONENTS="configs"    Installs program files and core configuration files
  .\WinFCU-x64-<version>.exe /COMPONENTS="examples"   Installs program files and example include files
  .\WinFCU-x64-<version>.exe /COMPONENTS="service"    Installs program files and installs WinFCU as service
```

You can combine components in a comma separated string

```
  .\WinFCU-x64-<version>.exe /COMPONENTS="configs,service"  Will installs program files and core configuration
                                                           files and finally install WinFCU as service
```

Other commandline options can be found at: <http://www.jrsoftware.org/ishelp/topic_setupcmdline.htm>
