# Maintainer: Ali Mousavi <ali.mousavi[at]gmail[dot]com>
pkgname=limoo
pkgver=1.3
pkgrel=2
pkgdesc="An image viewer using Qt, QML, C++."
url="http://getsilicon.org/limoo/"
arch=('x86_64' 'i686')
license=('GPLv3')
depends=('qt4' 'exiv2')
makedepends=('cmake')
conflicts=("${pkgname/-git}")
source=(http://getsilicon.org/download/${pkgname}/${pkgname}-src-${pkgver}.tar.gz)
md5sums=('27dc9d0b8f89a9aea31c9dff1e2f27c4')

build() {
  cd "${srcdir}/${pkgname}-src-${pkgver}"
  cmake . -DCMAKE_INSTALL_PREFIX=/usr \
          -DCMAKE_BUILD_TYPE=release   
  make
}

package() {
  cd "${srcdir}/${pkgname}-src-${pkgver}"
  make DESTDIR="${pkgdir}" install
}

# vim:set ts=2 sw=2 et:
