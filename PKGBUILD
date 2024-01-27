# SPDX-License-Identifier: AGPL-3.0
#
# Maintainer:   Adrien Wu <adrien.sf.wu@gmail.com>
# Contributor:  Pellegrino Prevete <cGVsbGVncmlub3ByZXZldGVAZ21haWwuY29tCg== | base -d>
# Contributor:  Truocolo <truocolo@aol.com>

_py="python2"
_pkg="decorator"
pkgbase="${_py}-${_pkg}"
pkgname=(
  "${pkgbase}"
)
pkgver=4.4.2
pkgrel=1
pkgdesc="Decorators for Humans"
url="https://github.com/micheles/${_pkg}"
arch=(
  'any'
)
depends=(
  "${_py}"
)
makedepends=(
  "${_py}-setuptools"
)
_pypi="https://files.pythonhosted.org/packages/source"
source=(
  "${_pypi}/${_pkg::1}/${_pkg}/${_pkg}-${pkgver}.tar.gz"
)
sha256sums=(
  'e3a62f0520172440ca0dcc823749319382e377f37f140a0b99ef45fecb84bfe7'
)

build() {
  cd \
    "${srcdir}/${_pkg}-${pkgver}"
  "${_py}" \
    setup.py \
      build
}

package() {
  cd \
    "${srcdir}/${_pkg}-${pkgver}"
  "${_py}" \
    setup.py \
      install \
      --root="${pkgdir}" \
      --optimize=1 \
      --skip-build
}

# vim:set sw=2 sts=-1 et:
