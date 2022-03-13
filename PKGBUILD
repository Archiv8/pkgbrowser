#!/bin/bash

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154
# ToDo: Add files: User documentation
# ToDo: Add files: Tooling
# FixMe: Namcap warnings and errors

# Maintainer: kachelaqa <kachelaqa at gmail dot com>
# Contributor: Ross Clark <archiv8@artisteducator.com>



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
depends=("pacman" "hicolor-icon-theme")
makedepends=("python-pyqt5")
# checkdepends=()
# optdepends=()
# provides=()
# conflicts=()
# replaces=()
# backup=()
# options=()
install="${pkgname}.install"
changelog="NEWS"
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
    "d808c073fa46aae56ebae14d5e16c06bc93142c4b21fb7c5e6e34e0f62f8407de400aa5aba931ca8a8fb03a9dc122018af910fa6cc8361c9dc81d2faf946a512"
    "9beabce4d52e48e4758ef570634d3fb268136a71615c53c922dab19a70f5dd48fa41d3a4033a312d35a3da40fb71b61df161e60cbb6828a37d89501885ef8899"
    "0cc9d1e43a5d367d722cf54ede15e2d771908d2550ba8b96778fe956d2530b18722de87c32873862a5282b2166dcbb7576650dd8b01aa83420ebc0c2c365f8d9"
    "ceae2f41752053520ef5ff91112ea54ca643996c648c16e4c8ffa126410f3cba8aac9b8c50da7d048673db0a6e7597c6c79396c12bae87ce247bff4a56322932"
    "970fb5584cb02033d6d592beda73153853f06fa433bff783fce73eb07684c3aae5e9f49f23bebf52970dedefdd84e491a3ee6ebaa6a46fb5803b1e4b418ce180"
    "f04bee3045e71788b6024569130a078fbacb4cd15944065fc9d23cbf2707458e1d93b45f5decdd7b17e4882a61b681c76b82c25416e795da4b6daefa3bbf4b4b"
    "11a286c5a97a0469f64a14e2b645891cbd36c017005ce05463f95552d886bbb8b7749c989fc3b27467505a0fd0b7c379325abae0a71d6a4cb9ae478be6b48da7"
    "28274fcc927de9e826dfb8d28f0428aefd3602601dc09112bcb22251d211cb4a323d1388495b4f153cb8c8e2b99cd024473c67a1c7ae2d7d9c1f712c2fa02802"
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
