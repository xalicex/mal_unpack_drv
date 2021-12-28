# mal_unpack_drv
MalUnpack companion driver

Works with: https://github.com/hasherezade/mal_unpack

**WARNING: This is an experimental version, use it on a Virtual Machine only!**

How to install
---

1. Enable testsigning on your Virtual Machine, where the driver will be installed:

```
bcdedit /set testsigning on
```

Then reboot the system...

2. Right click on `MalUnpackCompanion.inf` from the driver package. From the context menu, choose "Install"
3. Run the commandline as Administrator. Deploy the command:
```
fltmc load MalUnpackCompanion
```

How to unload
---
Run the commandline as Administrator. Deploy the command:
```
fltmc unload MalUnpackCompanion
```

Confirm that the driver is loaded
---

#### Option 1.

Run the commandline as Administrator. Deploy the command:
```
fltmc
```
You should see `MalUnpackCompanion` on the list of installed filter drivers.

#### Option 2.

Install Nirsoft DriversList (available [here](https://www.nirsoft.net/utils/installed_drivers_list.html)). Check if MalUnpackCompanion is on the list, and if it is running. This tool allows you also to easily check the current version of the installed driver.

How to use
---

Download the [`mal_unpack`](https://github.com/hasherezade/mal_unpack) userland application, and use it as it is mentioned in the instructions. If the MalUnpackCompanion driver is installed and loaded, the userland application will detect it automatically, and communicate with it.

