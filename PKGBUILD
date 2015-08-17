# Maintainer: kevku <kevku@gmx.com>
pkgname=python-librtmp-git
pkgver=33.96c978d
pkgrel=2
pkgdesc="Python interface to librtmp"
arch=('x86_64' 'i686')
url="https://github.com/chrippa/python-librtmp"
license=('Simplified BSD')
depends=('python>=3.4.0' 'python-cffi' 'rtmpdump')
makedepends=('python-setuptools')
provides=('python-librtmp')
conflicts=('python-librtmp')

source=("git://github.com/chrippa/python-librtmp.git")
sha256sums=('SKIP')
pkgver() {
	cd "$srcdir/python-librtmp"
	printf "%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	cd "$srcdir/python-librtmp"
	python setup.py build
}

package() {
	cd "$srcdir/python-librtmp"
	python setup.py install --root="$pkgdir/" --optimize=1
}
