## Which OpenStack am I running on?


```
$ sudo dmidecode | head -n30
# dmidecode 3.0
Getting SMBIOS data from sysfs.
SMBIOS 2.8 present.
9 structures occupying 436 bytes.
Table at 0x000F6880.

Handle 0x0000, DMI type 0, 24 bytes
BIOS Information
        Vendor: SeaBIOS
        Version: 1.10.2-1ubuntu1~cloud0
        Release Date: 04/01/2014
        Address: 0xE8000
        Runtime Size: 96 kB
        ROM Size: 64 kB
        Characteristics:
                BIOS characteristics not supported
                Targeted content distribution is supported
        BIOS Revision: 0.0

Handle 0x0100, DMI type 1, 27 bytes
System Information
        Manufacturer: OpenStack Foundation
        Product Name: OpenStack Nova
        Version: 17.0.6
        Serial Number: 452ca901-927a-4baa-9be9-9fa22d36b17c
        UUID: 46AFA4EE-FBA7-49EE-B491-FE7A028D2B88
        Wake-up Type: Power Switch
        SKU Number: Not Specified
        Family: Virtual Machine
```
