# $Id$

pkgname=glacier-browser
pkgver=0.2.1
pkgrel=1
pkgdesc="Nemo browser"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-browser"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt6-glacier-app' 'qt6-webengine')
makedepends=('cmake' 'qt6-tools' 'clang')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('fb4315f595584866f90607720dd5c7a50459408a75733c0a61d44fee0b5b1416')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make  all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
