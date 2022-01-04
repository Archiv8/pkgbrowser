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
depends=("pacman>=4.1" "pacman<6.1" "python>=3.2" "python<3.11" "python-pyqt5")
# makedepends=()
# checkdepends=()
# optdepends=()
# provides=()
# conflicts=()
# replaces=()
# backup=()
# options=()
install="${pkgname}.install"
# changelog=
source=(
    "https://osdn.net/dl/${pkgname}/${pkgname}-${pkgver}.tar.gz"
"CHANGELOG.md"
"COMMITLOG.md"
"INSTALL.md"
"ISSUES.md"
"LICENSE.md"
"MIT.md"
"README.md"
)
# noextract=()
sha512sums=(
    "191cea529f93f4f6674933561b861c4ee651a3fbe912d8c35310bb2a3c46a6f594275dd715bbe692a1d99a11a0e110546b8db05d41a02ca81e9a72d84bdc3c98"
            "ca62f601e3dbd3b03122d1f567a7d34210e8a1c35ef4f835a2e3ded1a9d041d2ee8278760c048ba7ed85decdd3ebc4904c821c4d4dc02aa69918013b723857ad"
            "d555ffa3bdcf27f7414fed10c67a56acc0622bd4c0fb10582bf9f5d91729df6c9e86d226289c713f965d9c69f1526209099bd4e9e86056a80015fbfa1f36dc0f"
            "31c57f3a8e1914acca710e7ffe8f1a399ec979dce79b8e7593ac926391e808573448c9395a2740cb1e63eb463ed0af351956c852805572b8df56c35ff7fb110a"
            "e1b953be98da16acee70f6cd97e881ece9745f364c5aeb700b551cdf18343351a24d72a0923653d443a1db1a2070a1ca663c1587061247798496f2d92a5254dc"
            "586f5af22536c8d7ce56fb4bdd526db9adc893bc04ea070be0c0f960a7f690722a51e7704f39af2818279936cc9daf75f7a9d8f2e0dde8e9234eeb00290b64ab"
            "e082a769e14e77e8021c494011e5e520499b44f7640919dffe3fa63aed87f40857573162085ad4a17bc1cfa1ec22462e3f1f52a79ec0fd03f1eeb0e21469044c"
            "b6c5ea948d7b5590b14570c1734e68ac8a38f28a169957bf129fbaa297fea459bc318924075bb4759699ee7be9767efb6f6bca4d3fcbc9702fa01aa62070c35b")
# validpgpkeys=()

build() {
    cd "${srcdir}/${pkgname}-${pkgver}" || printf "\n\n==> Error: Failed to find source code directory needed to build, %s. This is likely to be an error with the packaging:\n \n\e]8;;https://github.com/Archiv8/%s/issues/new?labels=priority: CRITICAL :clock1:,status: new :ear:,element: package :gift:,type: bug :bug:&title=[Archiv8: %s]  Missing+source+code+directory\e\\Please file an issue to help Archiv8 to continue to improve\e]8;;\e\\ \n\nHold the ctrl button whilst clicking the link to open an issue form\n\n\n" "${pkgname}" "${pkgname}" "${pkgname}"

    make PREFIX="/usr"
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}" || printf "\n\n==> Error: Failed to find source code directory needed to build, %s. This is likely to be an error with the packaging:\n \n\e]8;;https://github.com/Archiv8/%s/issues/new?labels=priority: CRITICAL :clock1:,status: new :ear:,element: package :gift:,type: bug :bug:&title=[Archiv8: %s]  Missing+source+code+directory\e\\Please file an issue to help Archiv8 to continue to improve\e]8;;\e\\ \n\nHold the ctrl button whilst clicking the link to open an issue form\n\n\n" "${pkgname}" "${pkgname}" "${pkgname}"

    make PREFIX="/usr" DESTDIR="${pkgdir}" install


}
