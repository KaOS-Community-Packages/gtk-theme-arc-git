pkgname=gtk-theme-arc-git
pkgver=549.d9d1772
pkgrel=1
pkgdesc='A flat theme with transparent elements for GTK 3, GTK 2 and Gnome-Shell. (git version)'
arch=('x86_64')
url="https://github.com/horst3180/arc-theme"
license=('GPL3')
depends=('gtk3' 'gtk-engine-murrine')
makedepends=('git')
source=("arc-theme::git+${url}.git")
sha256sums=('SKIP')

pkgver() {
    cd arc-theme
    echo "$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

build() {
    cd arc-theme
    ./autogen.sh --prefix=/usr
}

package() {
    make -C arc-theme DESTDIR="${pkgdir}" install
}
