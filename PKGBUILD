# Contributor: Kevin Piche <kevin@archlinux.org>
# Contributor: Andrew Wright <andreww@photism.org>

pkgname=gift-fasttrack
pkgver=0.8.9
pkgrel=5
pkgdesc="A FastTrack plugin for giFT."
arch=('i686' 'x86_64')
url="http://developer.berlios.de/projects/gift-fasttrack"
license=('GPL')
depends=('gift')
install=fasttrack.install
source=(http://download.berlios.de/${pkgname}/giFT-FastTrack-${pkgver}.tar.gz)
md5sums=('68521847537985bcc5e9b8677343374c')
options=(!libtool)

build() {
  cd ${srcdir}/giFT-FastTrack-${pkgver}
  ./configure --prefix=/usr || return 1
  make || return 1
  make DESTDIR=${pkgdir} install || return 1
}
