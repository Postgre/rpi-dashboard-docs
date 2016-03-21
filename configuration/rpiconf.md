# rpi.conf

This is the main configuration file. All settings are stored under **[GLOBAL]** section.
Below is a description of all options:

### DefaultAccess

Sets who has access to modules. Available options are:
* **guests**

  This option allows access to anyone who can reach the web service.

* **users**

  This option allows access to any user, who has a registered username and password in [rpi.users](rpiusers.md).

* **list**

  This option allows only users listed in **DefaultAllowedUsers** or overriden in [modules.conf](modulesconf.md) in **AllowedUsers**.

The effect of this option can be overriden for each module separately in [modules.conf](modulesconf.md).

    DefaultAccess users

By default the configuration is set to allow access to all users.

### DefaultAllowedUsers

List users that have access to modules, when **DefaultAccess** or overriden in [modules.conf](modulesconf.md) **Access** is set to **list**. Multiple users can be set, separated with spaces.

The effect of this option can be overriden for each module separately in [modules.conf](modulesconf.md).

    DefaultAllowedUsers admin

By default this option lists *admin* user.
