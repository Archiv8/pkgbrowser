# [Archiv8][a8-url] INSTALLATION GUIDE

_Exploring and Sharing Custom [Arch Linux][arch-url] PKGBUILDs_

[![Contributor Covenant, version 2.0.0, adopted][covenant-badge]][a8-contrib-covenant-url] [![Contributors License Agreement adopted][cla-badge]][a8-cla-url] [![Conventional Commits][commits-badge]](https://conventionalcommits.org)

---

[Readme](README.md) || [Install](INSTALL.md) || [Issues](ISSUES.md) || [Licensing](LICENSE.md) || [How to help](HOW-TO-HELP.md) || [CHANGELOG](Changelog.md)

---

_This repository contains unofficial packaging for an installation of [PkgBrowser][ups-pkg-url], a utility for browsing [pacman databases][arch-pkgs-url] and the [AUR][arch-aur-url]._ _**It is not affiliated, authorized, endorsed by, or in other way connected with either Arch Linux or the PkgBrowser project.**_

---

## Dependencies

There are no dependencies for [PkgBrowser][ups-pkg-url] that need to be made available prior to building and installing this package.

## Installation

Arch Linux provides different ways of building and installing packages. The simplist is annotated below, sourced from the [ArchWiki page on makepkg][arch-wiki-makepkg].

### Recommended installation route

Archiv8 recommends that you build the package in a clean chroot and add it to a local repository.

#### Setup the repository

```shell



```

#### Add the repository to /etc/pacmam.conf

#### Obtain the package

#### Build the package

Build the package using, for example, aur build from [aurutils package][aurutils-aur]

### makepkg

#### Obtain the package

**Option 1**:  (_preferred_) Clone the package from the Archiv8, [pkgbrowser repository][a8-pkg-gitclone]

```shell

Download the package from the Archiv8 repository

```

**Option 2**:  Download the package from the Archiv8, [pkgbrowser repository][a8-pkg-url]

```shell

cd /directory/to/the-package

```

If you downloaded the package it will need extracting

```shell

cd /directory/to/the/package

```

#### Build the package

Once the package is extracted or if the package was cloned change to the package director

```shell

makepkg -s

```

#### Install the package

```shell

makepkg -i

```

### Further resources

The following resources are available to assist building a package:

+ [Building in a clean chroot][buildchroot-arch-wiki]
+ [chroot][chroot-arch-wiki]
+ [proot package][proot-pkg-aur]
+ [proot arch wiki][proot-arch-wiki]
+ [proot help][proot-help-url]
+ [proot source][proot-url]
+ [fakechroot][fakechroot-url]
+ [fakechroot wiki][fakechroot-wiki]
+ [Arch Linux Package][fakechroot-pkg-url]
+ [aur utils][aurutils-aur]
+ [aurutils github][aurutils-github]
+ [Custom local repository][local-repo-arch-wiki]
+ Other tools that may be useful are listed on the [AUR helpers][arch-wiki-aurhelpers] page of the ArchWiki

---

[![Creative Commons Attribution-ShareAlike 4.0 International License][cc-large-badge]][cc-by-sa-url]

[Documentation for this project is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa-url]

Any original software produced for [Archiv8][a8-url] and / or quoted within the documentation is released under the MIT License

The license for upstream software, including the Arch Linux packaging tools used in the creation of this package, remains as designated by its creator and contributors

Thanks to those who have contributed to [Archiv8][a8-contrib-url]

(c) Documentation and Original Code, 2017 - 2022 Ross Clark and [Archiv8][a8-url]

_**Ross Clark and Archiv8 reserve the right to update or change the license for code or documentation under their ownership.  Notification of changes will appear in packages CHANGELOG.md**_

---

[![Code Released Under MIT License][mit-badge]][mit-url] [![Documentation Released Under Creative Commons, Attribution ShareAlike, 4.0.0 License][cc-badge]][cc-terms-url]

[cc-badge]: https://img.shields.io/badge/License-CC%20by%20SA%204.0.0-informational.svg
[cc-large-badge]: https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg
[cla-badge]: https://img.shields.io/badge/Adopted-Contributor%20%20License%20Agreement-brightgreengreen
[changelog-badge]: https://img.shields.io/badge/Keep%20a%20Changelog-1.1.0-informational
[commits-badge]: https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg
[covenant-badge]: https://img.shields.io/badge/Contributor%20Covenant-2.0.0-informational.svg
[mit-badge]: https://img.shields.io/badge/License-MIT-informational.svg
[semver-badge]: https://img.shields.io/badge/Semantic%20Versioning-2.0.0-informational.svg

[cc-by-sa-url]: https://creativecommons.org/licenses/by-sa/4.0/
[cc-compat-url]: http://creativecommons.org/compatiblelicenses
[cc-dev-consider-url]: https://wiki.creativecommons.org/wiki/Considerations_for_licensors_and_licensees#Considerations_for_licensors
[cc-policies-url]: http://creativecommons.org/policies
[cc-pub-consider-url]: https://wiki.creativecommons.org/wiki/Considerations_for_licensors_and_licensees#Considerations_for_licensees
[cc-pub-domain-url]: https://creativecommons.org/publicdomain/zero/1.0/legalcode
[cc-terms-url]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-url]: http://creativecommons.org/

[arch-aur-url]: https://aur.archlinux.org/
[arch-url]: https://www.archlinux.org/
[arch-pkgs-url]: https://archlinux.org/packages/
[arch-wiki-url]: https://wiki.archlinux.org

[a8-cc-by-sa-url]: https://archiv8.github.io/licences/creative-commons
[a8-cla-url]: https://archiv8.github.io/licenses/contributor-license-agreement
[a8-commits-url]: https://archiv8.github.io/contributing/style-guides/conventional-commits
[a8-conduct-url]: https://archiv8.github.io/community/code-of-conduct
[a8-contrib-covenant-url]: https://archiv8.github.io/community/code-of-conduct
[a8-contrib-people-url]: https://github.com/Archiv8/pkgbrowser/people
[a8-mit-url]: https://archiv8.github.io/licences/mit
[a8-pkg-url]: https://github.com/Archiv8/pkgbrowser
[a8-projects-url]: https://github.com/Archiv8
[a8-url]: https://archiv8.github.io/

[change-url]: https://keepachangelog.com
[commits-url]: https://conventionalcommits.org
[contrib-covenant-url]: https://osdn.net/projects/pkgbrowser/
[mit-url]: https://opensource.org/licenses/MIT
[semver-url]: https://semver.org
[ups-pkg-url]: https://osdn.net/projects/pkgbrowser/

[local-repo-arch-wiki]: https://wiki.archlinux.org/title/Pacman/Tips_and_tricks#Custom_local_repository
[aurutils-aur]: https://aur.archlinux.org/packages/aurutils
[aurutils-github]: https://github.com/AladW/aurutils
[buildchroot-arch-wiki]: https://wiki.archlinux.org/title/DeveloperWiki:Building_in_a_clean_chroot
[chroot-arch-wiki]: https://wiki.archlinux.org/title/Chroot
[fakechroot-pkg-url]: https://archlinux.org/packages/extra/x86_64/fakechroot/
[fakechroot-url]: https://github.com/dex4er/fakechroot
[fakechroot-wiki]: https://github.com/dex4er/fakechroot/wiki
[proot-arch-wiki]: https://wiki.archlinux.org/title/PRoot
[proot-help-url]: https://proot-me.github.io/
[proot-pkg-aur]: https://aur.archlinux.org/packages/proot/
[proot-url]: https://github.com/proot-me/proot
[ups-pkg-url]: https://osdn.net/projects/pkgbrowser/
