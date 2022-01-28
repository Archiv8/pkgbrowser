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
    "b568fb9bde84b1fb72011f4680a4a8a35ff5861a928e33aa2e352b9b8eaa4476a421fe759b087aa4b725f232693a46e1ba4198c417221066d7c76f2371f59688"
    "22c5d1af807d7333f31958f20a0bb40c220c83861a3df0fedbb9b0b9a5b7eb7216e2ff812cb4cd8ca58e3fb47743c1a4f9fc728fda1294dca22b14c329883568"
    "ecfe39fb9b7f3b7136b680b211d5fdd6e844609cf4e1aa5680b1234b04110f696ca05cb094a325e1770e31abb2197bae654419d8ce83adbd0a6745a071720320"
    "73d5328265797e76dc29ce38aefc92715df9b9e61f5d6e85be60cf65f07ecbdcec609b240d609865d945ffb19d9e536f60ee127f15d1be54a0867a0a291a0b75"
    "e869d31fb9818bd02ace66d13846a15047333509942acd84bf95f021743e5b0ccee54184d371d100adc5fe24f23384c798ce4b6d2e03fc13256bdb94bdefa501"
    "e7cc72b303f4c3532e7f8a705f4dda008e04ab9d729a8ab19cdae384e58c36cebd8f04de115074c068c8c9226f2d6ccfc89ab575fe2c69395404eb62bafddad0"
    "6356a196342f83b73e546c6331ede7d0211d9193d91e5b437cbebb1877764f43801c95c99c1060a32e167b4352584dc02060604acbc24258cc46c09643c34b9b"
     "0b07ac85bcd5e9529c673d804f39e309e6866acbac42164b6f9224dfde363476cacbfe939e50addb24654d37fdc2ae9a4459fe2d0d77bc406e71b9c7327dd81d"
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
