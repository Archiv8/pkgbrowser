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
#pkgdesc="A utility for browsing pacman databases and the AUR"
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
    "063daeab2d06a0d8a8474abbcf4d09c92d89db649fa7cf7df436eb252969344ec2e1a28d37531571deac74633a9d68cd78d306196e749b0fa93fc093ffaede06"
    "b6b58fdc1438abe13697d29b6680e21631fa8fec22527b14b8b865c72b96a7f5ba49257b2e93da48c301c9ad0b22d7cde195438ed72c8d7b1127d14dffdc76fd"
    "3ec49c014afc1a9ed22b5a656248feaabbe776afa330223cd7e1fda9a4dcd1f81cc7f98971e3593aa98c1843317899a0c8a792b49c47bcb2ec525c416c33170a"
    "1d324973063254f6fbe7fb35115744bb042cdeafb84a267f53bbd5f772d2e9a5f0bfa4b1a35e62fc407e759c44c6c0549682247e54983afbeb39f1f44b2edf86"
    "b2552d6f1e0bbd705b7c0e8bb6d27d0af4de81402e3235e880f6d850e2d75322e432fff6941bb8b4805432b98e313206d012037daa20890a20feee331ade9039"
    "d2ff032f5d762b4849add1528966e8bb8f37bb18f6b1269e3b667c53fcecf1a88be7508761b6aaa1bd5ebf014b9291ca78fe65adac137d96576088490f7b4e01"
    "5b7ae06e127b68f2969ed809a5d61ca8dbadac69e764eb235d61eae768b17b7982bcaddda77044a883eda5715f603289992548c6bedd6cd4809e3518f8675b05"
    "038c6ce873525cb00527c49968ab38d95c23a85e406bab1616504ea491f499413a1102acb90568ca6852bff7cb8aa28a6c306ec5f76f15994634d0a5f8f87a55"
    "68d98ade3415d535e6ecef6408b0588fe75611285b871b96c6df46704c0615ec482e1461b64fbaf2bd7386f98b6ee208afd36aab99ed9a6a56f425daaf895733"
)
# validpgpkeys=()

build() {
    cd "${srcdir}/${pkgname}-${pkgver}" || printf "\n\n==> Error: Failed to find source code directory needed to build, %s. This is likely to be an error with the packaging:\n \n\e]8;;https://github.com/Archiv8/%s/issues/new?labels=priority: CRITICAL :clock1:,status: new :ear:,element: package :gift:,type: bug :bug:&title=[Archiv8: %s]  Missing+source+code+directory\e\\Please file an issue to help Archiv8 to continue to improve\e]8;;\e\\ \n\nHold the ctrl button whilst clicking the link to open an issue form\n\n\n" "${pkgname}" "${pkgname}" "${pkgname}"

    make PREFIX="/usr"
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}" || printf "\n\n==> Error: Failed to find source code directory needed to build, %s. This is likely to be an error with the packaging:\n \n\e]8;;https://github.com/Archiv8/%s/issues/new?labels=priority: CRITICAL :clock1:,status: new :ear:,element: package :gift:,type: bug :bug:&title=[Archiv8: %s]  Missing+source+code+directory\e\\Please file an issue to help Archiv8 to continue to improve\e]8;;\e\\ \n\nHold the ctrl button whilst clicking the link to open an issue form\n\n\n" "${pkgname}" "${pkgname}" "${pkgname}"

    make PREFIX="/usr" DESTDIR="${pkgdir}" install

    # Create Archiv8 documentation folder
    install -dvm 755 "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/"
    install -dvm 755 "${pkgdir}/usr/share/licenses/${pkgname}/Archiv8/"

    # Install Archiv8 related documentation
    install -Dm 644 "${srcdir}/CC-BY-SA-V4.md" "${pkgdir}/usr/share/licenses/${pkgname}/Archiv8/CC-BY-SA-V4.md"
    install -Dm 644 "${srcdir}/CHANGELOG.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/CHANGELOG.md"
    install -Dm 644 "${srcdir}/HOW-TO-HELP.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/HOW-TO-HELP.md"
    install -Dm 644 "${srcdir}/INSTALL.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/INSTALL.md"
    install -Dm 644 "${srcdir}/ISSUES.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/ISSUES.md"
    install -Dm 644 "${srcdir}/LICENSE.md" "${pkgdir}/usr/share/licenses/${pkgname}/Archiv8/LICENSE.md"
    install -Dm 644 "${srcdir}/MIT.md" "${pkgdir}/usr/share/licenses/${pkgname}/Archiv8/MIT.md"
    install -Dm 644 "${srcdir}/README.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/README.md"
}
