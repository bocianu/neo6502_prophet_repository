# Neo6502 Software Repository for Prophet Server/Client Infrastructure

[Neo6502](https://www.neo6502.com/) is a modern open-source hardware and software retro computer featuring a W65C02 processor and RP2040. Software is stored on a USB flash drive (or SD card), and while you can manually download it, if you have a [Wi-Fi module](https://www.olimex.com/Products/IoT/ESP8266/MOD-WIFI-ESP8266/open-source-hardware) connected to your UEXT port, you can use the [Prophet client](https://gitlab.com/bocianu/neo-prophet) to download programs directly to your Neo6502 storage.

This repository is intended to contain all available software for the Neo6502 that is legally distributable through this system. While this may be a temporary solution, and I may switch to something more sophisticated in the future, it serves our needs for now.

I will strive to keep the repository updated periodically, adding new software that appears on the channels I monitor. If you can assist in maintaining this software base, your help would be greatly appreciated. Below, I will briefly explain how to add or update existing entries. However, if this process seems too complex, feel free to [send me a message](mailto:bocianu@gmail.com) with the files you’d like to publish, and I’ll handle it for you.

## Directory Structure

The main folder contains category folders. You can create a new category simply by adding a new folder. Inside category folders, there are package folders and optionally a **desc.yaml** file. This file can include additional metadata describing the category details.

Available fields for categories:

```yaml
name: Optional category name - defaults to the category folder name.
description: Optional description of the category.
```

Each category can contain any number of packages. A package can be a single file or multiple files (up to 64). Currently, subdirectories within packages are not supported, but this may be improved in the future.

Within a package directory, you can also include a **desc.yaml** file with additional metadata. This file has more available fields:

```yaml
id: Unique identifier (a single word without spaces). Defaults to the package folder name with spaces replaced by underscores.
title: Full title of the package (defaults to the folder name).
description: Detailed description of the package and its content.
author: Author's name.
date: Release date.
version-number: Software version number.
folder-name: Installation folder name (defaults to the package folder name).
screenshots: Optional list of screenshots.
changelog: Short description of changes since the last version.
tags: Optional list of tags.
```

## Package Versioning

You can store multiple versions of the same package using subfolders within the package directory. Any subfolder starting with an underscore followed by a number (e.g., '_0', '_33') can contain an older version of the package that can optionally be installed. Similar to the folders above, version folders can (and should) also include a **desc.yaml** file with specific fields:

```yaml
author: Author's name.
date: This version's release date.
version-number: This version number.
folder-name: Installation folder name (defaults to the package folder name).
screenshots: Optional list of screenshots.
changelog: Short description of changes since the last version.
```
#### WARNING: Package versioning must be supported by the client software to function correctly!

---
