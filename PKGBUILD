pkgname=glacier-settings-developermode
pkgver=0.1.1
pkgrel=1
pkgdesc="Nemo developer mode"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/$pkgname"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt6-glacier-app' 'glacier-settings')
makedepends=('cmake' 'qt6-tools' 'clang')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('709ea6b91c2e4d1e62993786e42abc58f1e4d6baefa5b1633ca731cbb7623932')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
