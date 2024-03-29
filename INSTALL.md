# [Archiv8][a8]![External Link][ext-link_h1] INSTALLATION GUIDE

_Exploring and Sharing Custom [Arch Linux][arch]![External Link][ext-link] PKGBUILDs_

[![Contributor Covenant, version 2.0.0, adopted][covenant-badge]][a8-community-covenant]![External Link][ext-link_h2] [![Contributors License Agreement adopted][cla-badge]][a8-community-cla]![External Link][ext-link_h2] [![License: Apache V.20][apache-badge]][license-apache-a8]![External Link][ext-link_h2] [![License: CC BY-SA 4.0][cc-badge]][license-cc-a8]![External Link][ext-link_h2]

---

_This repository contains unofficial packaging for an installation of [PkgBrowser][ups-pkg]![External Link][ext-link], a utility for browsing [pacman databases][arch-pkgs]![External Link][ext-link] and the [AUR][arch-aur]![External Link][ext-link]_

_**It is not affiliated, authorized, endorsed by, or in other way connected with either Arch Linux or the PkgBrowser project**_

---

[Readme](README.md) || ![Page Indicator][nav-r-em][Install](INSTALL.md)![Page Indicator][nav-l-em] || [Issues](ISSUES.md) || [Community](COMMUNITY.md) || [How to Help](HOW-TO-HELP.md) || [Change Log](CHANGELOG.md) || [License](LICENSE.md)

---

## Getting the PkgBrowser build files

Download the [latest release][a8-pkg-src]![External Link][ext-link] containing the PKGBUILD and associated files.

## Dependencies

There are no Archiv8 / AUR dependencies for [PkgBrowser][ups-pkg]![External Link][ext-link] that need to be made available prior to building and installing this package.

## Installation

Installation should should follow one of the methods described in the [ArchWiki][arch-wiki-aur]![External Link][ext-link].  If you are building many Archiv8 / AUR packages creating and using a [custom local repository][arch-wiki-local-repo]![External Link][ext-link] will help speed up the process.

### makepkg

[Makepkg][archwiki-makepkg]![External Link][ext-link] is possibly the simplest method to build and install a package.  It will handle the dependencies available from the [Official Arch Linux Repositories][arch-pkgs]![External Link][ext-link] and those that have already been installed

```shell

makepkg -si

```

### Clean chroot

Archiv8's preferred method to build and install a package is in a [clean chroot][archwiki-buildchroot]![External Link][ext-link].  It helps to prevent dependency issues and diagnose build errors. An alternative to building and using the chroot as described on the ArchWiki is [aurutils][aurutils-github]![External Link][ext-link] an create a custom local repository

## More information

_**Further instructions for [building][a8-docs-build]![External Link][ext-link] and [installing][a8-docs-install]![External Link][ext-link] packages are available on the [Archiv8 website][a8-docs]![External Link][ext-link] or [ArchWiki][arch-wiki]![External Link][ext-link]**_

Any issues encountered when building or installing this package should be reported in the [PkgBrowser repository][a8-issue-pkg].

---

---

Report issues about this [document][a8-issue-doc]![External Link][ext-link],  [licensing][a8-issue-license]![External Link][ext-link] or [attribution][a8-issue-attrib]![External Link][ext-link] via the github repository

---

The license for upstream software, including the Arch Linux packaging tools used in the creation of this package, remains as designated by its creator and contributors

Thanks to those who have contributed to [Archiv8][a8-contrib-people]![External Link][ext-link] and [this package in particular][a8-contrib-pkg-people]![External Link][ext-link]

---

---

[cc-badge]: https://img.shields.io/badge/License-CC_BY--SA_4.0-lightgrey.svg
[cc-large-badge]: https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg
[cla-badge]: https://img.shields.io/badge/Adopted-Contributor%20%20License%20Agreement-brightgreengreen
[changelog-badge]: https://img.shields.io/badge/Keep%20a%20Changelog-1.1.0-informational
[commits-badge]: https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg
[covenant-badge]: https://img.shields.io/badge/Contributor%20Covenant-2.0.0-informational.svg
[apache-badge]: https://img.shields.io/badge/License-Apache_2.0-blue.svg
[mit-badge]: https://img.shields.io/badge/License-MIT-informational.svg
[semver-badge]: https://img.shields.io/badge/Semantic%20Versioning-2.0.0-informational.svg

[a8-logo]: image_A8-logo.svg

[ext-link]: image_ext-link.svg
[ext-link_h1]: image_ext-link_h1.svg
[ext-link_h2]: image_ext-link_h2.svg
[ext-link_h2]: image_ext-link_lrg.svg

[nav-r-em]: image_arrow-right_emphasis.svg
[nav-l-em]: image_arrow-left_emphasis.svg
[nav-r]: image_arrow-right.svg
[nav-l]: image_arrow-left.svg

[license-apache-in]: /APACHE-V2.0-FULL.md
[license-apache-out]: http://www.apache.org/licenses/LICENSE-2.0
[license-apache-a8]: https://archiv8.github.io/licensing/apache-v2-0-full

[license-cc-short-out]: https://creativecommons.org/licenses/by-sa/4.0/
[license-cc-long-out]: https://creativecommons.org/licenses/by-sa/4.0/legalcode
[license-cc-a8]: https://archiv8.github.io/licensing/creative-commons
[license-cc-in]: /CC-BY-SA-4.0.md
[license-cc-compat]: http://creativecommons.org/compatiblelicenses
[license-cc-dev-consider]: https://wiki.creativecommons.org/wiki/Considerations_for_licensors_and_licensees#Considerations_for_licensors
[license-cc-policies]: http://creativecommons.org/policies
[license-cc-pub-consider]: https://wiki.creativecommons.org/wiki/Considerations_for_licensors_and_licensees#Considerations_for_licensees
[license-cc-pub-domain]: https://creativecommons.org/publicdomain/zero/1.0/legalcode
[license-cc-terms]: http://creativecommons.org/licenses/by-sa/4.0/
[license-cc]: http://creativecommons.org/

[license-mit-in]: /MIT.md
[license-mit-a8]: https://archiv8.github.io/licensing/mit
[license-mit-out]: https://opensource.org/licenses/MIT

[change]: https://keepachangelog.com
[commits]: https://conventionalcommits.org
[contrib-covenant]: https://www.contributor-covenant.org/
[semver]: https://semver.org

[arch]: https://www.archlinux.org/
[arch-aur]: https://aur.archlinux.org/
[arch-pkgs]: https://archlinux.org/packages/
[arch-wiki]: https://wiki.archlinux.org
[arch-wiki-aur]: https://wiki.archlinux.org/title/Arch_User_Repository
[arch-wiki-local-repo]: https://wiki.archlinux.org/title/Pacman/Tips_and_tricks#Custom_local_repository
[arch-wiki-makepkg]: https://wiki.archlinux.org

[a8]: https://archiv8.github.io/
[a8-changelog]: https://archiv8.github.io/contributing/style-guides/changelog
[a8-commits]: https://archiv8.github.io/contributing/style-guides/ccommits
[a8-community-cla]: https://archiv8.github.io/community/cla
[a8-community-covenant]: https://archiv8.github.io/community/contributor-covenant
[a8-community-guide]: https://archiv8.github.io/community/guidelines
[a8-contrib-people]: https://archiv8.github.io/people
[a8-contrib-pkg-people]: https://github.com/Archiv8/pkgbrowser/people
[a8-docs]: https://archiv8.github.io/docs
[a8-docs-build]: https://archiv8.github.io/docs/build
[a8-docs-install]: https://archiv8.github.io/docs/install
[a8-docs-update]: https://archiv8.github.io/docs/update
[a8-pkg-src]: https://github.com/Archiv8/pkgbrowser/releases/latest
[a8-projects]: https://github.com/Archiv8

[ups-pkg]: https://osdn.net/projects/pkgbrowser/

[archwiki-aur]: https://wiki.archlinux.org/title/Arch_User_Repository
[archwiki-aur-helpers]: https://wiki.archlinux.org/title/AUR_helpers
[archwiki-aur-tug]: https://wiki.archlinux.org/title/AUR_Trusted_User_Guidelines
[archwiki-buildchroot]: https://wiki.archlinux.org/title/DeveloperWiki:Building_in_a_clean_chroot
[archwiki-chroot]: https://wiki.archlinux.org/title/Chroot
[archwiki-local-repo]: https://wiki.archlinux.org/title/Pacman/Tips_and_tricks#Custom_local_repository
[archwiki-makepkg]: https://wiki.archlinux.org/title/Makepkg
[archwiki-pkg-guidelines]: https://wiki.archlinux.org/title/Arch_package_guidelines
[archwiki-proot]: https://wiki.archlinux.org/title/PRoot

[aur]: https://aur.archlinux.org/

[aurutils-github]: https://github.com/AladW/aurutils
[aurutils-pkg-aur]: https://aur.archlinux.org/packages/aurutils
[aurutils-pkg-a8]: https://github.com/Archiv8/pkgbrowser

[fakechroot-pkg]: https://archlinux.org/packages/extra/x86_64/fakechroot/
[fakechroot-github]: https://github.com/dex4er/fakechroot
[fakechroot-wiki]: https://github.com/dex4er/fakechroot/wiki

[aurutils-pkg-aur]: https://aur.archlinux.org/packages/aurutils
[aurutils-pkg-a8]: https://github.com/Archiv8/pkgbrowser
[aurutils-pkg-github]: https://github.com/AladW/aurutils
[proot-pkg-aur]: https://aur.archlinux.org/packages/proot/
[proot-pkg-a8]: https://github.com/Archiv8/proot/
[proot-github]: https://github.com/proot-me/proot
[proot-help]: https://proot-me.github.io/

[a8-issue]: https://github.com/Archiv8/pkgbrowser/issues/new/choose
[a8-issue-app]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+app+%3Acomputer%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+LOW+%3Aok_hand%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_APP.yml&title=%5BAPPLICATION%5D%3A+Add+brief+description+here
[a8-issue-com]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+community+%3Afamily%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+CRITICAL+%3Aclock1%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_COMMUNITY.yml&title=%5BCOMMUNITY%5D%3A+Add+brief+description+here
[a8-issue-doc]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+doc+%3Aledger%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+NORMAL+%3Acalendar%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_DOC.yml&title=%5BDOCUMENTATION%5D%3A+Add+brief+description+here&page-name=pkgbrowser\INSTALL.md
[a8-issue-form]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+form+%3Ascroll%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+NORMAL+%3Acalendar%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_FORM.yml&title=%5BFORM%5D%3A+Add+brief+description+here
[a8-issue-license]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element:+license+:scroll:,status:+new+:phone:,priority:+NORMAL+:calendar:,wait:+triage+:hospital:&template=FORM_OTHER.yml&title=[LICENSE]:+Add+brief+description+here
[a8-issue-attrib]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element:+license+:scroll:,status:+new+:phone:,priority:+NORMAL+:calendar:,wait:+triage+:hospital:&template=FORM_OTHER.yml&title=[ATTRIBUTION]:+Add+brief+description+here
[a8-issue-other]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+other+%3Aquestion%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+NORMAL+%3Acalendar%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_OTHER.yml&title=%5BOTHER%5D%3A+Add+brief+description+here
[a8-issue-pkg]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+package+%3Agift%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+CRITICAL+%3Aclock1%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_PACKAGE_ISSUE.yml&title=%5BPACKAGE+ISSUE%5D%3A+Add+brief+description+here&package-name=PkgBrowser
[a8-issue-out]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+package+%3Agift%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+CRITICAL+%3Aclock1%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_PACKAGE_OUTDATED.yml&title=%5BOUTDATED+PACKAGE%5D%3A+Add+brief+description+here
[a8-issue-req]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+package+%3Agift%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+CRITICAL+%3Aclock1%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_PACKAGE_REQUEST.yml&title=%5BPACKAGE+REQUEST%5D%3A+Add+brief+description+here
[a8-issue-ups]: https://github.com/Archiv8/pkgbrowser/issues/new?assignees=rossclarkartist&labels=element%3A+src+%3Aspeedboat%3A%2Cstatus%3A+new+%3Aphone%3A%2Cpriority%3A+NORMAL+%3Acalendar%3A%2Cwait%3A+triage+%3Ahospital%3A&template=FORM_UPSTREAM.yml&title=%5BUPSTREAM%5D%3A+Add+brief+description+here
[a8-issue-sec]: https://github.com/Archiv8/pkgbrowser/security/policy
