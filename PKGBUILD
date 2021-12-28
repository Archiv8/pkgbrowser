#!/bin/bash

# Maintainer: kachelaqa <kachelaqa at gmail dot com>
# Contributor: Ross Clark <contact@artisteducator.com>

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the 
# repository root directory, see https://github.com/koalaman/shellcheck/wiki 
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154

# pkgbase=""
pkgname='pkgbrowser'
pkgdesc='A utility for browsing pacman databases and the AUR'
pkgver=0.25
pkgrel=2
# epoch=
url="https://osdn.net/projects/$pkgname"
license=('GPL2')
arch=('x86_64')
# groups=()
depends=('pacman>=4.1' 'pacman<6.1' 'python>=3.2' 'python<3.11' 'python-pyqt5')
# makedepends=()
# checkdepends=()
# optdepends=()
# provides=()
# conflicts=()
# replaces=()
# backup=()
# options=()
install="$pkgname.install"
# changelog=
source=("https://osdn.net/dl/$pkgname/$pkgname-$pkgver.tar.gz")
# noextract=()
sha512sums=('191cea529f93f4f6674933561b861c4ee651a3fbe912d8c35310bb2a3c46a6f594275dd715bbe692a1d99a11a0e110546b8db05d41a02ca81e9a72d84bdc3c98')
# validpgpkeys=()

build() {
    cd "$srcdir/$pkgname-$pkgver"
    make PREFIX='/usr'
}

package() {
    cd "$srcdir/$pkgname-$pkgver"
    make PREFIX='/usr' DESTDIR="$pkgdir" install
}
