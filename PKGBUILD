#!/bin/bash

# Based on the original PKGBUILD and associated files by kachelaqa <kachelaqa at gmail dot com>

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# [ToDo]: Add files: User documentation
# [ToDo]: Add files: Tooling
# [FixMe]: Namcap warnings and errors. Do these need clearning up?
# [FixMe]: PKGBUILD (pkgbrowser) W: Reference to x86_64 should be changed to $CARCH
# [FixMe]: pkgbrowser W: Referenced library 'pkgbrowser' is an uninstalled dependency

# Maintainer: Ross Clark <https://github.com/Archiv8/pkgbrowser/discussions>
# Contributor: Ross Clark <https://github.com/Archiv8/pkgbrowser/discussions>

_realname="PkgBrowser"

# pkgbase=""
pkgname="pkgbrowser"
pkgdesc="A utility for browsing pacman databases and the AUR"
pkgver=0.27
pkgrel=3
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
  # [Note]: Required but installed through other dependencies
  # "python"
  "python-poppler-qt5"
  "python-qscintilla-qt5"
  # [Note]: Required but installed through other dependencies
  # "python-pyqt5"
  "python-pyqt5-3d"
  "python-pyqt5-datavisualization"
  "python-pyqt5-networkauth"
  "python-pyqt5-purchasing"
  "python-pyqt5-webengine"
  "python-pyqt5-chart"
  # [Note]: Required but installed through other dependencies
  # "hicolor-icon-theme"
)
# makedepends=(

# )
# checkdepends=()
# optdepends=()
# provides=()
# conflicts=()
# replaces=()
# backup=()
# options=()
# [Query]: Does not seem to be needed as runs a command provided by hooks
# install="${pkgname}.install"
#changelog="NEWS"
source=(
  "https://osdn.net/dl/${pkgname}/${pkgname}-${pkgver}.tar.gz"
)
# noextract=()
sha512sums=(
  "238bcecfe7e4f46af2909df3d82cc4259982691c540c45db0ee8f535b3f282510ffdd423b4911bbfb143c91b1eb8b392c1f9de49ac98830842bf01c9f20d0223"
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
}
