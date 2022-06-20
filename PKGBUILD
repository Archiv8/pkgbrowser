#!/bin/bash

# Based on the original PKGBUILD and associated files by kachelaqa <kachelaqa at gmail dot com>

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# [ToDo]: Add files: User documentation
# [ToDo]: Add files: Tooling
# [FixMe]: Namcap warnings and errors

# Maintainer: Ross Clark <https://github.com/Archiv8/pkgbrowser/discussions>
# Contributor: Ross Clark <https://github.com/Archiv8/pkgbrowser/discussions>

_realname="PkgBrowser"

# pkgbase=""
pkgname="pkgbrowser"
pkgdesc="A utility for browsing pacman databases and the AUR"
pkgver=0.27
pkgrel=2
# epoch=
url="https://osdn.net/projects/${pkgname}"
license=(
  "GPL2"
)
arch=(
  "x86_64"
)
# groups=()
depends=(
  "pacman"
  "hicolor-icon-theme"
)
makedepends=(
  "python-pyqt5"
)
# checkdepends=()
# optdepends=()
# provides=()
# conflicts=()
# replaces=()
# backup=()
# options=()
install="${pkgname}.install"
#changelog="NEWS"
source=(
  "https://osdn.net/dl/${pkgname}/${pkgname}-${pkgver}.tar.gz"
  "CHANGELOG.md"
  "HOW-TO-HELP.md"
  "INSTALL.md"
  "ISSUES.md"
  "README.md"
  "image_A8-logo.svg"
  "image_arrow-left_emphasis.svg"
  "image_arrow-left.svg"
  "image_arrow-right_emphasis.svg"
  "image_arrow-right.svg"
  "image_ext-link_h1.svg"
  "image_ext-link_h2.svg"
  "image_ext-link_lrg.svg"
  "image_ext-link.svg"
)
# noextract=()
sha512sums=(
  "238bcecfe7e4f46af2909df3d82cc4259982691c540c45db0ee8f535b3f282510ffdd423b4911bbfb143c91b1eb8b392c1f9de49ac98830842bf01c9f20d0223"
  "a849eb63590fd46745c521bff9af215dc01c5ab4f1ca4b04c55b85e935a79c358143ae1a2043f2d0242785e9610807ce419f34190bb33368c5d9a8d2a9e01d96"
  "c827f968917812d0cfcdb43389dc13a9c6380f28e65e92d3ebc6713f468dd2545e5a983734f9d957a4a86d87857b1b42966b2842b85f475ca9e698fef7f22e2d"
  "04b595e872272c61509f6f6aacce09a7af37aebd9e827430316857bcf39a55780354667e7499f3db2ba4a5ebfa3834996a8b257aa5976e4cf1ac8ba7e06f7fa3"
  "4af5ed455fde7e7cdbb9dae1b9dcda5b70654b651e521b1c49291a1330caed302102e8c4565c485b8aca3ce17daedec94df3bfb6ffd14875ac2bf14ea24d73b2"
  "5e9ad0c4709a33faae35a8270223049646d4c4077b5062732a3deee8509ee928a16aca4aa013fc34cd1e8b9f90d70e0eb045ccac5fda4770b7201e792d267d65"
  "2b32bb0e8dcc993df9f2f5fb0b53651c22173800fce37e88daa1701c0fad4b0defb9a4a9170f634eca2a03a51dda69e3e9ebb597d4f42c2e63b3bc73855d2426"
  "0514efbb26fc798d6865482ae8a0b6760b0abfe1bccd88741aa49d52a151f153204c7b0101b0f60eb3c9e27d2cdb27fa081f32713d3d8396b46c0f54cb7d7cb7"
  "2a0960558090b4b06a6cefd8ce61c1ab5c24fffb9ef0aab09f80b37c6eaf3936d9ce7babfa3f6002872c2e2d82f715fcd1d74a9872e3212c4748ff19920bbedb"
  "21e18c4d80fb1a3d709c3483903b7975bc9f6eb7cf7fe31a9b7c6eea2d98d99a4c2463ddbc2973d3369b5d14bf498659f6488c8f9ed6c2f42258649f93946d76"
  "e17146a1a3a8820d4d07b392ed8901b23dc93e1d9534159f6c673cddf76c303e91aaa5cb24cb4427062b64a3654bae4e714dfbd200e745ec0704be011b14c050"
  "f64078216739a1fb6c2ec2f9eb31bcaa31a8d089735ab3c6e2acac792eabfb4d5359383fdd5d79b27716628ea01a0cacb29f57ec138d4b46873ed6a34e6e779b"
  "2b4622b50ef3dd7ac80f7abe92618d9b11f4f7aa3e9f6eefd90a07b7c7f119a796943a06baf57c03270bcf5b511db8bb4d56c457c23dc6e1b1b1600d9e0b0347"
  "2559bb8198cabbf6a534be764277c6b9101a20b539d6ae4ae4689c2c38d672e70f228118865950de317facda4ce126b63499b7eb6d5b4799359203064c0634c6"
  "658272178948c414d129508e2e536daa8a5f1cd106b7e2f95e9159dfb35cdb617d72ad0cb911ea1b70e45fb82fbb37b4397baefde416110435d25e02691b79aa"
)
# validpgpkeys=()

build() {

  cd "${srcdir}/${pkgname}-${pkgver}" || printf "\n\e[31;1m==> ERROR:\e[1m Failed to find the source code directory needed to build %s\n\e[0m \e[31;1m > \e[0m\e]8;;https://github.com/Archiv8/%s/issues/new?labels=priority: CRITICAL :clock1:,status: new :ear:,element: package :gift:,type: issue :bug:,wait: triage :hospital:&title=[Archiv8: %s] Missing+source+code+directory\e\\Please report the issue on GitHub\e]8;;\e\\ \n \e[31;1m >\e[0m Tip: Hold ctrl and click the link above to open the form in your browser\n\n" "${_realname}" "${pkgname}" "${pkgname}"

  make PREFIX="/usr"
}

package() {

  cd "${srcdir}/${pkgname}-${pkgver}" || printf "\n\e[31;1m==> ERROR:\e[1m Failed to find the source code directory needed to build %s\n\e[0m \e[31;1m > \e[0m\e]8;;https://github.com/Archiv8/%s/issues/new?labels=priority: CRITICAL :clock1:,status: new :ear:,element: package :gift:,type: issue :bug:,wait: triage :hospital:&title=[Archiv8: %s] Missing+source+code+directory\e\\Please report the issue on GitHub\e]8;;\e\\ \n \e[31;1m >\e[0m Tip: Hold ctrl and click the link above to open the form in your browser\n\n" "${_realname}" "${pkgname}" "${pkgname}"

  make PREFIX="/usr" DESTDIR="${pkgdir}" install

  install -Dm 644 "${srcdir}/${pkgname}-${pkgver}/doc/manual.html" "${pkgdir}/usr/share/doc/${pkgname}/manual.html"

  install -Dm 644 "${srcdir}/${pkgname}-${pkgver}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

  # Create Archiv8 documentation folder
  install -dvm 755 "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/"

  # Install documentation images Archiv8 documentation folder
  install -Dm 644 "${srcdir}/image_A8-logo.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_A8-logo.svg"
  install -Dm 644 "${srcdir}/image_arrow-left_emphasis.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_arrow-left_emphasis.svg"
  install -Dm 644 "${srcdir}/image_arrow-left.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_arrow-left.svg"
  install -Dm 644 "${srcdir}/image_arrow-right_emphasis.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_arrow-right_emphasis.svg"
  install -Dm 644 "${srcdir}/image_arrow-right.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_arrow-right.svg"
  install -Dm 644 "${srcdir}/image_ext-link_h1.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_ext-link_h1.svg"
  install -Dm 644 "${srcdir}/image_ext-link_h2.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_ext-link_h2.svg"
  install -Dm 644 "${srcdir}/image_ext-link_lrg.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_ext-link_lrg.svg"
  install -Dm 644 "${srcdir}/image_ext-link.svg" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/image_ext-link.svg"

  # Install Archiv8 related documentation
  install -Dm 644 "${srcdir}/CHANGELOG.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/CHANGELOG.md"
  install -Dm 644 "${srcdir}/HOW-TO-HELP.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/HOW-TO-HELP.md"
  install -Dm 644 "${srcdir}/INSTALL.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/INSTALL.md"
  install -Dm 644 "${srcdir}/ISSUES.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/ISSUES.md"
  install -Dm 644 "${srcdir}/README.md" "${pkgdir}/usr/share/doc/${pkgname}/Archiv8/README.md"
}
