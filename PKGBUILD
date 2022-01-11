#!/bin/bash

# Maintainer: kachelaqa <kachelaqa at gmail dot com>
# Contributor: Ross Clark <contact@artisteducator.com>

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154

# pkgbase=""
pkgname="pkgbrowser"
pkgdesc="A utility for browsing pacman databases and the AUR"
pkgver=0.25
pkgrel=2
# epoch=
url="https://osdn.net/projects/${pkgname}"
license=("GPL2")
arch=("x86_64")
# groups=()
depends=("pacman>=4.1" "pacman<6.1" "python>=3.2" "python<3.11" "python-pyqt5" "hicolor-icon-theme")
# makedepends=()
# checkdepends=()
# optdepends=()
# provides=()
# conflicts=()
# replaces=()
# backup=()
# options=()
install="${pkgname}.install"
changelog="CHANGELOG.md"
source=(
    "https://osdn.net/dl/${pkgname}/${pkgname}-${pkgver}.tar.gz"
    "CC-BY-SA-V4.md"
    "CHANGELOG.md"
    "HOW-TO-HELP.md"
    "INSTALL.md"
    "ISSUES.md"
    "LICENSE.md"
    "MIT.md"
    "README.md"
)
# noextract=()
sha512sums=(
    "191cea529f93f4f6674933561b861c4ee651a3fbe912d8c35310bb2a3c46a6f594275dd715bbe692a1d99a11a0e110546b8db05d41a02ca81e9a72d84bdc3c98"
    "36c321325e718005d65185bfde0b8bd6ffa87af11a0c44254d26abdb81b018405291767b3b3853cb0e83ba510d1828b7a1eeb3573a113f724155fd0e593df4b2"
    "c78c999c108502cb368a3d602365fecf6e4c683d890f12bfaa364b970118fbd979c8bbbc365074c2903700d112050602105f98d1d9839a1724f382912862ff82"
     "5cd4dca33b3ce7f55c5a87faccc127f1fcb57ce1bb20525e27b47746d2bc6fad2e9af745dcf1b7605d262a36c566d2f6919e7c7d12e503234f7a75ac397d482a"
     "12f4b1dad5d5ff06bbb81ae7dca49c0d76937bf624aa1e96fb866bfb3b3a633a70460590554525c1993a0bcb35fae669fb7a90626d745a299759b7e2da176514"
      "d6719acaa366e3169d48cade72afe7c91fc324a6286aafd9fbe78d27e05cdb5a400bac90b00251e15f2771e9d472a374956a300f55972d37ef68456ca6e2a240"
     "b5c18eb83da7f1676e27a02b8c10d21383f8ebcd8e0380474fd47f908a23219b4e47d4b91eae8fdd1076d1bbbfed16f48ba601b1640489844e8a3aa4a61156c9"
    "9c8226d68bc7dfde0bde0a9071273463dd33477fb25dcd046a0b0513f066a6b647556678039e3f0784ac2cd96017682537a19b1cb468c6583f5468d04dea0fa7"
    "9dd4bc62082544c936caa1f9c41f30b42f99614d804cc34afdc06b5061fe9d622170221d1942751c7b078e91cafb0aac7e088cd174c8c6d5ccd59a67a96fac4c"
)
# validpgpkeys=()

build() {
    cd "${srcdir}/${pkgname}-${pkgver}" || printf "\n\n==> Error: Failed to find source code directory needed to build, %s. This is likely to be an error with the packaging:\n \n\e]8;;https://github.com/Archiv8/%s/issues/new?labels=priority: CRITICAL :clock1:,status: new :ear:,element: package :gift:,type: bug :bug:&title=[Archiv8: %s]  Missing+source+code+directory\e\\Please file an issue to help Archiv8 to continue to improve\e]8;;\e\\ \n\nHold the ctrl button whilst clicking the link to open an issue form\n\n\n" "${pkgname}" "${pkgname}" "${pkgname}"

    make PREFIX="/usr"
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}" || printf "\n\n==> Error: Failed to find source code directory needed to build, %s. This is likely to be an error with the packaging:\n \n\e]8;;https://github.com/Archiv8/%s/issues/new?labels=priority: CRITICAL :clock1:,status: new :ear:,element: package :gift:,type: bug :bug:&title=[Archiv8: %s]  Missing+source+code+directory\e\\Please file an issue to help Archiv8 to continue to improve\e]8;;\e\\ \n\nHold the ctrl button whilst clicking the link to open an issue form\n\n\n" "${pkgname}" "${pkgname}" "${pkgname}"

    make PREFIX="/usr" DESTDIR="${pkgdir}" install

    install -Dm 644 "${srcdir}/${pkgname}-${pkgver}/doc/manual.html" "${pkgdir}/usr/share/docs${pkgname}/manual.html"

    install -Dm 644 "${srcdir}/${pkgname}-${pkgver}/LICENSE" "${pkgdir}/usr/share/license/${pkgname}/LICENSE"

    # Create Archiv8 documentation folder
    install -dvm 755 "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/"

    # Install Archiv8 related documentation
    install -Dm 644 "${srcdir}/CC-BY-SA-V4.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/CC-BY-SA-V4.md"
    install -Dm 644 "${srcdir}/CHANGELOG.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/CHANGELOG.md"
    install -Dm 644 "${srcdir}/HOW-TO-HELP.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/HOW-TO-HELP.md"
    install -Dm 644 "${srcdir}/INSTALL.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/INSTALL.md"
    install -Dm 644 "${srcdir}/ISSUES.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/ISSUES.md"
    install -Dm 644 "${srcdir}/LICENSE.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/LICENSE.md"
    install -Dm 644 "${srcdir}/MIT.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/MIT.md"
    install -Dm 644 "${srcdir}/README.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/README.md"
}
