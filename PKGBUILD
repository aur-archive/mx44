# Maintainer: David Adler <david dot jo dot adler at gmail dot com>
pkgname=mx44
_pkgname=Mx44
pkgver=2
pkgrel=4
pkgdesc="polyphonic multi-channel MIDI software synthesizer"
arch=(i686 x86_64)
url="http://web.comhem.se/luna/"
license=('GPL')
depends=('jack' 'gtk2')
source=(http://web.comhem.se/luna/$_pkgname.$pkgver.tar.gz)
md5sums=('8e532c78d79e189fe5b6e2dd10acf0e2')

build() {
  cd $srcdir/$_pkgname.$pkgver/src
  make
}

package() {
  cd $srcdir/$_pkgname.$pkgver/src
  install -m755 -d ${pkgdir}/usr/bin
  make PREFIX=$pkgdir/usr/ install
}

# vim:set ts=2 sw=2 et:
