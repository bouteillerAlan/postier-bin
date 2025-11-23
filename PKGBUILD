# Maintainer: Bouteiller a2n Alan <a2n.dev@pm.me>
pkgname=postier-bin
appname=postier
pkgver=2.0.0
pkgrel=2
pkgdesc="API client without bloat"
arch=('x86_64')
url="https://github.com/results-may-vary-org/postier"
license=('GPL')
depends=('glibc' 'gtk3' 'webkit2gtk-4.1' 'desktop-file-utils' 'hicolor-icon-theme')
options=('!strip' '!emptydirs')
install=${pkgname}.install
source_x86_64=("${url}/releases/download/v"${pkgver}"/"${appname}"_"${pkgver}"_amd64.deb")
sha256sums_x86_64=('e3d11a22ed1cdb5c117ca1f1b9b5666a4019afb9889315515c7fe6823bb9004e')
package() {
  # Extract the deb package
  ar x "${appname}_${pkgver}_amd64.deb"

  # Extract package data
  tar -xz -f data.tar.gz -C "${pkgdir}"

  # Fix permissions
  chmod 755 "${pkgdir}/usr/bin/tape"
}
