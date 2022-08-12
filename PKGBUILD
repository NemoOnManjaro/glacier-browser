# $Id$

pkgname=glacier-browser
pkgver=0.1.2
pkgrel=1
pkgdesc="Nemo browser"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-browser"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt5-glacier-app' 'qt5-webengine')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('aa9e795cff9aba5c9bf55e67f6306a96993269e9a2f4e8602b0e035e89571fe9')

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
