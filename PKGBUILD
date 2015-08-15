# Maintainer: Limao Luo <luolimao+AUR@gmail.com>
# Contributor: dorphell <dorphell@archlinux.org>
# Contributor: Judd Vinet <jvinet@zeroflux.org>

_pkgname=expat
pkgname=$_pkgname-libtool
pkgver=2.1.0
pkgrel=1
pkgdesc="An XML Parser library written in C"
arch=(i686 x86_64)
url=http://$_pkgname.sourceforge.net/
license=(MIT)
depends=($_pkgname=$pkgver)
options=(libtool)
source=(http://downloads.sourceforge.net/sourceforge/$_pkgname/$_pkgname-$pkgver.tar.gz)
sha256sums=('823705472f816df21c8f6aa026dd162b280806838bb55b3432b0fb1fcca7eb86')
sha512sums=('2a9ad2b44b87b84087979fe4114d661838df3b03dbdcb74d590cb74096bf35ce9d5a86617b0941a2655ea441a94537bcbcd78252da92342238823be36de2d09d')

build() {
    cd $_pkgname-$pkgver/
    ./configure --prefix=/usr --mandir=/usr/share/man
    make
}

package() {
    install -Dm644 $_pkgname-$pkgver/libexpat.la "$pkgdir"/usr/lib/libexpat.la
}
