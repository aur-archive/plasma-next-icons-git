# Maintainer: Phoenix Nemo <phoenixlzx at archlinuxcn.org>

_gitname=plasma-next-icons
pkgname=plasma-next-icons-git
pkgver=94f9ba8
pkgrel=1
pkgdesc="the early work on the next KDE icon theme"
arch=('any')
url=https://github.com/NitruxSA/plasma-next-icons
license=('GPLv3')
makedepends=(git)
source=($_gitname::git://github.com/NitruxSA/plasma-next-icons.git)
sha256sums=('SKIP')

pkgver() {
  cd "$pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/$_gitname"
  install -d ${pkgdir}/usr/share/icons
  install -Dm644 ${srcdir}/${_gitname}/LICENSE ${pkgdir}/usr/share/licenses/${_gitname}/LICENSE
  cp -r ${srcdir}/${_gitname}/{Breeze,"Breeze Dark"} ${pkgdir}/usr/share/icons/
}

