# Maintainer: SpepS <dreamspepser at yahoo dot it>
# Contributor: dorphell <dorphell@archlinux.org>
# Contributor: Tom Newsom <Jeepster@gmx.co.uk>

pkgname=joe
pkgver=3.7
pkgrel=3
pkgdesc="JOE has the feel of most IBM PC text editors"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/joe-editor"
license=('GPL')
depends=('ncurses')
optdepends=('gpm: console mouse support')
backup=('etc/joe/ftyperc' 'etc/joe/jicerc.ru' 'etc/joe/jmacsrc' \
        'etc/joe/joerc' 'etc/joe/jpicorc' 'etc/joe/jstarrc' 'etc/joe/rjoerc')
source=("http://downloads.sourceforge.net/joe-editor/$pkgname-$pkgver.tar.gz")
md5sums=('66de1b073e869ba12abbfcde3885c577')
sha1sums=('54398578886d4a3d325aece52c308a939d31101d')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure \
	--prefix=/usr \
	--sysconfdir=/etc \
	--mandir=/usr/share/man

  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir/" install
}
