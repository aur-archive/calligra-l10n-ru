# Russian localization for Calligra
# maintainer (i686): Konstantin Krasavin <konstantin[dot]hard[at]gmail[dog]com>
# maintainer (x86_64): Konstantin Krasavin <konstantin[dot]hard[at]gmail[dog]com>

pkgname=('calligra-l10n-ru')
pkgver=2.4.1
pkgrel=1
pkgdesc="Russian localization for Calligra"
arch=('any')
url="http://www.calligra-suite.org"
license=('LGPL')
makedepends=('cmake' 'automoc4' 'kdelibs' 'docbook-xsl')
source=(ftp://ftp.kde.org/pub/kde/stable/calligra-${pkgver}/calligra-l10n/calligra-l10n-ru-${pkgver}.tar.bz2)               
md5sums=('5e5bfcda98e2c3d105d336095a9c729e')

build() {
  cd $srcdir/$pkgname-$pkgver
  [[ -d build ]] && rm -r build
  mkdir build && cd build
  cmake \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DCMAKE_BUILD_TYPE=RelWithDebInfo \
    ..
  make
}
 
package() {
  cd $srcdir/$pkgname-$pkgver/build
  make DESTDIR=$pkgdir install
}
