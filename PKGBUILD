# Maintainer: Bouteiller a2n Alan <a2n.dev@pm.me>
pkgname=postier-bin
appname=postier
pkgver=2.0.0
pkgrel=3
pkgdesc="API client without bloat"
arch=('x86_64')
url="https://github.com/results-may-vary-org/postier"
license=('GPL')
depends=('glibc' 'gtk3' 'webkit2gtk-4.1' 'desktop-file-utils' 'hicolor-icon-theme')
options=('!strip' '!emptydirs')
install=${pkgname}.install
source_x86_64=("${url}/releases/download/v"${pkgver}"/"${appname}"_"${pkgver}"_amd64.deb")
sha256sums_x86_64=('b077b708b427b2b5e3b93d62562c903891a47f48d80c01651e8c67dd5642e63a')
package() {
  # Extract the deb package
  ar x "${appname}_${pkgver}_amd64.deb"

  # Extract package data
  tar -xz -f data.tar.gz -C "${pkgdir}"

  # Fix permissions
  chmod 755 "${pkgdir}/usr/bin/postier"
}
