pkgname=konsole-gruvbox-git
pkgver=r150
pkgrel=1
pkgdesc="gruvbox color scheme for KDE konsole"
arch=('x86_64')
url="https://github.com/morhetz/gruvbox-contrib.git"
license=('MIT')
depends=('konsole')
makedepends=('git')
source=("$pkgname::git+$url")
md5sums=('SKIP')

pkgver() {
	cd "$pkgname"

	# use number of revisions as version
	printf "r%s" "$(git rev-list --count HEAD)"
}

package() {
    install -Dm644 "${srcdir}/${pkgname}/konsole/Gruvbox_dark.colorscheme" "${pkgdir}/usr/share/konsole/Gruvbox_dark.colorscheme"
}
