# $Id$

pkgname=glacier-browser
pkgver=0.2
pkgrel=1
pkgdesc="Nemo browser"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-browser"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt6-glacier-app' 'qt6-webengine')
makedepends=('cmake' 'qt6-tools' 'clang')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('3b8acc3639f5fd9e4f67c44ecf2bee53d97279f6f9a4889ee3b26682d52ebee0')

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
