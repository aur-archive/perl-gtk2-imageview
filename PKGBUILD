# Maintainer:  TDY <tdy@archlinux.info>
# Contributor: Olaf Leidinger <leidola@newcon.de>

pkgname=perl-gtk2-imageview
pkgver=0.05
pkgrel=3
pkgdesc="Perl bindings to the GtkImageView image viewer widget"
arch=('i686' 'x86_64')
url="http://search.cpan.org/dist/Gtk2-ImageView/"
license=('LGPL3')
depends=('cairo-perl>=1.00' 'glib-perl' 'gtk2-perl' 'gtkimageview>=1.6.0')
makedepends=('perl-extutils-depends' 'perl-extutils-pkgconfig')
options=('!emptydirs')
source=(http://search.cpan.org/CPAN/authors/id/R/RA/RATCLIFFE/Gtk2-ImageView-$pkgver.tar.gz)
md5sums=('7c961071b347b6a64b8351fdd87ec4c0')

build() {
  cd "$srcdir/Gtk2-ImageView-$pkgver"
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
  make
}

package() {
  cd "$srcdir/Gtk2-ImageView-$pkgver"
  make DESTDIR="$pkgdir" install
}
