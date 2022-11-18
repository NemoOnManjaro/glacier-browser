# $Id$

pkgname=glacier-browser
pkgver=0.1.3
pkgrel=1
pkgdesc="Nemo browser"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-browser"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt5-glacier-app>=0.9'
	'qt5-webengine')

makedepends=('qt5-tools' 'cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('f8cb21f2f953c3633690879bca8b1e7532fc65f9cbc1d00196da0b460821c2d9')

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
