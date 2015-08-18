# Maintainer: Belosoukinski Jacques <shingo-san@live.jp>
pkgname=x-blasterdominator-x64-beta
appname=x-blasterdominator-beta
pkgver=0
pkgrel=2
epoch=
pkgdesc="A vertical scrolling shoot'em up 2D"
arch=('x86_64')
url="http://injection-studio.com"
license=('privative')
install=${pkgname}.install
depends=('sfml')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=('x-blasterdominator-beta', 'x-blasterdominator-x64-beta')
source=('http://injection-studio.com/download/x-blasterdominator/beta-0.2/linux/x-blasterdominator-x64-beta.tar')
md5sums=('b528d74e63359a6249fb048c52781e64') #generate with 'makepkg -g'

package() {
	cd "$srcdir/$pkgname-$pkgver"
	mkdir -p "${pkgdir}"/usr/share/${appname}
	
	# Binary
	install -Dm 755 ${appname} "${pkgdir}/usr/share/${appname}"

	# Data
	cp -r content "${pkgdir}/usr/share/${appname}"

	# Desktop file
	install -Dm 644 x-blasterdominator-beta.desktop \
	"$pkgdir/usr/share/applications/x-blasterdominator-beta.desktop"

	# Icons
  	for _i in 32 48 64 128; do
    	install -Dm 644 icons/${appname}-${_i}x${_i}.png \
      	"$pkgdir/usr/share/icons/hicolor/${_i}x${_i}/apps/${appname}.png"
  	done

}
