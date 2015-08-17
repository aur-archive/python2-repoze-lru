# Maintainer : SpepS <dreamspepser at yahoo dot it>
# Contributor: DasIch <dasdasich@googlemail.com>

_name=repoze.lru
pkgname=python2-repoze-lru
pkgver=0.4
pkgrel=1
pkgdesc="A tiny LRU cache implementation and decorator"
arch=('any')
license=('custom:BSD')
url="http://pypi.python.org/pypi/$_name"
depends=('python2')
makedepends=('python2-distribute')
provides=("python2-$_name")
conflicts=("python2-$_name")
replaces=("python2-$_name")
source=(http://pypi.python.org/packages/source/r/$_name/$_name-$pkgver.tar.gz)
md5sums=('9f6ab7a4ff871ba795cadf56c20fb0f0')

build() {
  cd "$srcdir/$_name-$pkgver"
  python2 setup.py build
}

package() {
  cd "$srcdir/$_name-$pkgver"
  python2 setup.py install --root="${pkgdir}"

  # license
  install -Dm644 LICENSE.txt \
    "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
