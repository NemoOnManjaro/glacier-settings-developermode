pkgname=glacier-settings-developermode
pkgver=0.0.3
pkgrel=1
pkgdesc="Nemo developer mode"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/$pkgname"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt5-glacier-app' 'glacier-settings')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('fa545923d6900e9f128f5cd46f14d317ffbcc2a2287d545e410e10e9ce3c14c9')

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
