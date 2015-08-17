pkgname=ubase
pkgver=0.1
pkgrel=1
pkgdesc="A collection of tools similar in spirit to util-linux but much simpler"
url="http://tools.suckless.org/ubase"
arch=('i686' 'x86_64')
license=('MIT')
source=('http://dl.suckless.org/ubase/ubase-0.1.tar.gz')
md5sums=('38a7a1f1d66b53d4c55f17e01ee3fa44')

build() {
	cd "$srcdir/$pkgname-$pkgver"
	make
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	make PREFIX=/opt/ubase MANPREFIX=/opt/ubase/man DESTDIR="$pkgdir" install 
	install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
	install -m644 -D README "$pkgdir/usr/share/doc/$pkgname/README"
}
