# Maintainer: Felipe Magno de Almeida <felipe.m.almeida__at__gmail.com>

pkgbase=depanneur
pkgname=depanneur
pkgver=20160615
pkgrel=1
pkgdesc="Tizen's Depanneur project"
arch=('i686' 'x86_64')
license=('GPL')
makedepends=('perl')
depends=('perl' 'perl-yaml' 'perl-html-template' 'perl-json' 'perl-build')
source=('git://git.tizen.org/tools/depanneur.git' 'fixes.patch')
sha256sums=('SKIP' '0284b42be48bb6b4345d5dd62489d9d7e0fb0590ebd48baece2525a5e7b0a9a2')

build() {
  cd $srcdir/depanneur
  patch -p1 -i ../../fixes.patch
}

package() {
  cd $srcdir/depanneur
  DESTDIR=$pkgdir make install
#  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
