DaData.ru hints for OpenCart
================================

Description
---------------

The module displays hints by name and postal address, and also automatically determines the postal code on the registration and ordering page in OpenCart using the "Hints" service [DaData.ru] (https://dadata.ru).

! [Hints at address 1] (doc / dadata-opencart-demo-2.png)
! [Hints at address 2] (doc / dadata-opencart-demo-3.png)

According to online stores, the module significantly improves the quality of data received from users. Clients begin to indicate postal addresses for delivery, broken down by KLADR, without typos and with apartments, the index is determined automatically. Full name is entered without typos and with gender.
 
OpenCart 1.5.6.x.
OcStore 1.5.5.x.

Installation
---------

### 1. Install the module

First of all, download the [distribution] (hhttps: //github.com/hflabs/suggestions-opencart/releases/latest), unpack it, and copy the files from the `upload` directory to the root of the opencart store.

To replace the regions of Russia with the correct values ​​from the KLADR, run the SQL script `zone.sql` above the store database via phpMyAdmin or from the console:

``
$ mysql opencart -u opencart -p <zone.sql
``

### 2. Turn on hints in settings

The module is configured in the admin panel at: * Add-ons> Modules> DaData *.

! [Module settings] (doc / dadata-opencart-admin.png)

* API-key * - must be obtained in the [personal account] (https://dadata.ru/profile/#info) DaData.ru.

* Number of hints returned * - the number of hints that are shown to the user.

The remaining customization fields (auto-correct as you type, show additional address fields, show gender) control the behavior of the prompts. You can enable them as needed.

* Status * - shows the status of the module: "enabled" - the tips work, "disabled" - the tips do not work.

* Hints version * - which service to use when working (for more details see [Hints versions] (https://dadata.ru/suggestions/#pricing)).

After filling in all the fields, you must save the settings.

#### Settings for working with the simple checkout module

To select the correct region - set the Russian Federation as the default country in the module settings * Simple Checkout> Fields> country_id> Default value *

### 3. Use the hints!

Hints work when you enter your full name and address during registration and ordering:

! [Hints by name] (doc / dadata-opencart-demo-1.png)
! [Hints at address 1] (doc / dadata-opencart-demo-2.png)
! [Hints at address 2] (doc / dadata-opencart-demo-3.png)


Change history
-----------------
* 1.3
 * Added support for OcStore
* 1.2
 * Added support for simplecheckout (thanks to [deeman] (https://opencartforum.com/user/16563-deeman/))

* 1.1
 * Added the ability to use the paid version of the service
 * Rewrote the module code - you no longer need to edit the store source code.
 
* 1.0
 * First release 
