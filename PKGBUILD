# Contributor: Jakub Luzny <limoto94@gmail.com>
# Maintainer: SanskritFritz (gmail)

pkgname=sl
pkgver=5.02
pkgrel=2
pkgdesc='Steam Locomotive runs across your terminal when you type "sl" as you meant to type "ls".'
arch=('i686' 'x86_64' 'arm')
url="http://www.tkl.iis.u-tokyo.ac.jp/~toyoda/index_e.html"
license=('free')
depends=('ncurses')
source=("https://github.com/mtoyoda/sl/archive/$pkgver.tar.gz")

build() {
	cd "$srcdir/sl-$pkgver"

	cc $CFLAGS -o sl sl.c -lcurses
	gzip -9 -f sl.1
}

package() {
	cd "$srcdir/sl-$pkgver"

	install -Dm 775 sl "$pkgdir/usr/bin/sl"
	install -Dm 644 sl.1.gz "$pkgdir/usr/share/man/man1/sl.1.gz"
}

#category: games
# vim:set ts=2 sw=2 et:

md5sums=('5d5fe203eb19598821647ba8db5dde6c')
