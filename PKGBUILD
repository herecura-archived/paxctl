# Contributors:
#   sh0 <mee@sh0.org>
#   s1gma <s1gma@mindslicer.com>
#   henning mueller <henning@orgizm.net>

pkgname='paxctl'
pkgver='0.7'
pkgrel=2
pkgdesc='Manages various PaX related program header flags for Elf32, Elf64, binaries'
url='http://pax.grsecurity.net'
arch=('i686' 'x86_64')
license=('GPL')
depends=()
source=("http://pax.grsecurity.net/$pkgname-$pkgver.tar.bz2")

prepare() {
  cd "${pkgname}-${pkgver}"
  sed -i 's:/sbin:/usr/bin:' Makefile
}

build() {
  cd "${pkgname}-${pkgver}"
  make
}

package() {
  cd "${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}

sha256sums=('f7077784ca5695bf74061e6f66b86db855e0dcaa1fc94e6251f6ecd0b879cdc8')
