# [Archiv8][a8-url] CHANGE LOG

_Exploring and Sharing Custom [Arch Linux][arch-url] PKGBUILDs_

[![Contributor Covenant, version 2.0.0, adopted][covenant-badge]](CODE-OF-CONDUCT.md) [![Developer Certificate of Origin, version 1.1.0, adopted][certificate-badge]](DEVELOPER-CERTIFICATE-OF-ORIGIN.md)

---

[Readme](README.md) || [Install](INSTALL.md) || [Issues](ISSUES.md) || [Licensing](LICENSE.md) || [How to help](HOW-TO-HELP.md) || [Changelog](CHANGELOG.md)

---

_**This repository contains unofficial packaging for an installation of [PkgBrowser][ups-pkg-url], a utility for browsing pacman databases and the AUR.**_

_**It is not affiliated, authorized, endorsed by, or in other way connected with either Arch Linux or the PkgBrowser project.**_

_**The copyright holder reserves the right to update or change the licensing for the contents of this repository as required.**_

---

## Unreleased: (Items that have not being accepted yet)

## Latest: (Update without SHA, as is most recent update)

+ Regenerate .SRCINFO file
+ Update SHA's in PKGBrowser
+ Update change log

## :shower: 2022-01-11 | 13:57 | [5ebe917][5ebe917]

+ Update PKGBUILD by:
  + Uncommenting the package description (pkgdesc) pkgdesc variable
  + Add hicolor-icon-theme to dependencies as suggested by namcap
  + Updating SHAs to reflect recent file changes
  + Add upstream license and documentation to install
  + Install all Archiv8 documents to single directory to prevent broken links

## :wrench: 2022-01-11 | 13:57 | [7b9abe4][7b9abe4]

+ Add new line to end of file

## :wrench: 2022-01-11 | 13:57 | [88b153d][88b153d]

+ Correct upstream URL

## :phone: 2022-01-11 | 13:35 | [8020b97][8020b97]

+ Added suggested apps and links to start developing the install file as a useful
reference.

## :wrench: 2022-01-09 | 14:06 | [3734ddb][3734ddb]

+ Correct CHANGELOG to Changelog in menus

## :toolbox: 2022-01-09 | 12:17 | [c987205][c987205]

+ Remove unneeded links in files as packages can't use conventional change logs and commits
  + references to conventional commits
  + references to keep a change log
  + menu items referring to commit log
+ Make change log current with all commits
+ Remove commit log

## :toolbox: 2022-01-08 | 19:54 | SHA: [5b966c2][5b966c2]

+ Begin to add changes to file.

## :satellite: 2022-01-04 | 20:30 | SHA: [7636c61][7636c61]

+ Add auto-generated .SRCINFO file

## :phone: 2022-01-04 | 20:24 | SHA: [5c776de][5c776de]

+ Update docs to assist with user interaction
  + Add "HOW-TO-HELP.md" to document menu
  + Convert HTML markup back to Markdown after find replace error
  + Add reserves the right to change copyright
  + Add informative footer across all documents

## :phone: 2022-01-04 | 20:20 | SHA: [123f318][123f318]

+ Add file to how to help document to assist community building.

## :toolbox: 2022-01-04 | 20:17 | SHA: [854d018][854d018]

+ Add prettier lint files as placeholders

## :wrench: 2022-01-04 | 20:14 | SHA: [ad30098][ad30098]

+ .editorconfig
  + Updated created and last update dates

## :toolbox: 2022-01-04 | 20:08 | SHA: [2e74560][2e74560]

+ Add README type files for inclusion in installation

## :hash: 2022-01-04 | 10:44 | SHA: [3646d70][3646d70]

+ Add new integrity checks for files to PKGBUILD

## :shower: 2022-01-04 | 10:44 | SHA: [1dddc85][1dddc85]

+ Tidy files and add markdownlint rules
  + Added path to markdownlint configuration file
  + Updated and corrected external links:
    + Removed Gitter link in preparation for using GitHub discussions
    + Added link to upstream package
  + Added information for users:
    + Added non-affiliation statement
  + Tidied file to make more legible when rendered:
    + Validated links
    + Updated links to placeholders for easier updates

## :shower: 2022-01-04 | 10:20 | SHA: [38b7056][38b7056]

Tidy file add markdownlint rules

+ Added path to markdownlint configuration file
+ Updated and corrected external links:
  + Removed Gitter link in preparation for using GitHub discussions
  + Corrected link to upstream package
+ Added information for users:
  + Added non-affiliation statement
+ Tidied file to make more legible when rendered:
  + Reverted document markup to markdown where possible
  + Added <strong> to license list items where missing
  + Added <hr> between license sections
  + Removed unnecessary numbering on lists

## :shower: 2022-01-04 | 10:17 | SHA: [c2ccc0e][c2ccc0e]

+ Add markdown linting rules

## :shower: 2021-12-30 | 15:46 | SHA: [303ca6c][303ca6c]

+ Tidy vars to follow style guide.
  + Consistent use of double quotes to match style guide
  + Add failsafe to build() function so if "cd" fails there is more information
  + And a  message with URL to encourage user to report message.

## SHA: [5d5f81a][5d5f81a]

+ Tidy vars to follow style guide.
  + Tidied variables, by adding curly braces, to ensure common style across repositories
  + Add failsafe to build() function so if "cd" fails there is more information
  + And a  message with URL to encourage user to report message.

## :tada: 2021-12-28 | 16:30 | SHA: [4669e11][4669e11]

+ Initial upload to repository

---

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Documentation for this project is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

Any original software produced for [Archiv8][a8-url] and / or quoted within the documentation is released under the MIT License.

The license for upstream software, including the Arch Linux packaging tools used in the creation of this package, remains as designated by its creator and contributors.

Thanks to those who have contributed to [Archiv8][a8-contrib-url]

(c) Documentation and Code, 2017 - 2022 Ross Clark and [Archiv8][a8-url]

---

[![Code Released Under MIT License][mit-badge]][mit-url] [![Documentation Released Under Creative Commons, Attribution ShareAlike, 4.0.0 License][cc-badge]][cc-terms-url]

[cc-compat-url]: http://creativecommons.org/compatiblelicenses
[cc-dev-consider-url]: https://wiki.creativecommons.org/wiki/Considerations_for_licensors_and_licensees#Considerations_for_licensors
[cc-policies-url]: http://creativecommons.org/policies
[cc-pub-consider-url]: https://wiki.creativecommons.org/wiki/Considerations_for_licensors_and_licensees#Considerations_for_licensees
[cc-pub-domain-url]: https://creativecommons.org/publicdomain/zero/1.0/legalcode
[cc-terms-url]: http://creativecommons.org/licenses/by-sa/4.0/

[cc-badge]: https://img.shields.io/badge/License-CC%20by%20SA%204.0.0-informational.svg
[certificate-badge]: https://img.shields.io/badge/Developer%20Certificate%20of%20Origin-1.1.0-informational.svg
[changelog-badge]: https://img.shields.io/badge/Keep%20a%20Changelog-1.1.0-informational
[commits-badge]: https://img.shields.io/badge/Conventional%20Commits-1.0.0-informational.svg
[covenant-badge]: https://img.shields.io/badge/Contributor%20Covenant-2.0.0-informational.svg
[mit-badge]: https://img.shields.io/badge/License-MIT-informational.svg
[semver-badge]: https://img.shields.io/badge/Semantic%20Versioning-2.0.0-informational.svg

[arch-url]: https://www.archlinux.org/

[a8-url]: https://archiv8.github.io/
[a8-pkg-url]: https://github.com/Archiv8/pkgbrowser
[a8-contrib-url]: https://github.com/Archiv8/pkgbrowser/people

[change-url]: https://keepachangelog.com
[commits-url]: https://conventionalcommits.org
[mit-url]: https://opensource.org/licenses/MIT
[semver-url]: https://semver.org
[ups-pkg-url]: https://osdn.net/projects/pkgbrowser/

[5ebe917]: https://github.com/Archiv8/pkgbrowser/commit/5ebe917f5ca6840a1707fb407131efb10fa47225
[7b9abe4]: https://github.com/Archiv8/pkgbrowser/commit/7b9abe4d91d003f4e3d42038bb47972210df1aa2
[88b153d]: https://github.com/Archiv8/pkgbrowser/commit/88b153d461baf547dc099b109b8771d3b331c38b
[8020b97]: https://github.com/Archiv8/pkgbrowser/commit/8020b973f0ce933ca823a309631c52d62ee82ec5
[3734ddb]: https://github.com/Archiv8/pkgbrowser/commit/3734ddbda48641ddaa43cfff9f91a4e94d708931
[c987205]: https://github.com/Archiv8/pkgbrowser/commit/c98720541e963fa8a5a63c4277802c390c0ab47d
[5b966c2]: https://github.com/Archiv8/pkgbrowser/commit/5b966c247ae8f25a1e8f8dd986e2c2923bd8f148
[7636c61]: https://github.com/Archiv8/pkgbrowser/commit/7636c61700ab39e4d81ec322bc5dca2b4fd6b4ce
[5c776de]: https://github.com/Archiv8/pkgbrowser/commit/5c776dec9735c8a59137b4ecf18f85210548777c
[5c776de]: https://github.com/Archiv8/pkgbrowser/commit/5c776dec9735c8a59137b4ecf18f85210548777c
[123f318]: https://github.com/Archiv8/pkgbrowser/commit/123f318fd1fad18eda85ce1d0fa79f0f86856588
[854d018]: https://github.com/Archiv8/pkgbrowser/commit/854d018c2b6cdfe939f39e79af85ef00133bc2d1
[ad30098]: https://github.com/Archiv8/pkgbrowser/commit/ad300982ac0f63e25b8516ae7368e38f70d79286
[2e74560]: https://github.com/Archiv8/pkgbrowser/commit/2e745602e91ab6cda1672f749418db7add149007
[3646d70]: https://github.com/Archiv8/pkgbrowser/commit/3646d70acdb9bf3f7e2d7d314eb7cc0fd94b7cd3
[1dddc85]: https://github.com/Archiv8/pkgbrowser/commit/1dddc858a34f38126587c1e18c804431f850ecdf
[38b7056]: https://github.com/Archiv8/pkgbrowser/commit/38b7056815c03d3dcf61e9a02c414d670dcae024
[c2ccc0e]: https://github.com/Archiv8/pkgbrowser/commit/c2ccc0ebe852941021a0555bf5f5331f05eecccf
[303ca6c]: https://github.com/Archiv8/pkgbrowser/commit/303ca6cfbfa17687ea63130872af005606e6f455
[5d5f81a]: https://github.com/Archiv8/pkgbrowser/commit/5d5f81a8d946ca87b0aa72b629a2cfe4957897a2
[4669e11]: https://github.com/Archiv8/pkgbrowser/commit/4669e118e56bfd8eb8401a7776f2e61ca8b1e063
