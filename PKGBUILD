# Maintainer: João Reis <joaosreis@outlook.pt>
pkgname=tee-clc
pkgver=14.118.0
pkgrel=1
epoch=
pkgdesc="Microsoft Visual Studio Team Explorer Everywhere - command-line client for Visual Studio 2012 Team Foundation Server"
arch=(i686 x86_64)
url="https://github.com/Microsoft/team-explorer-everywhere"
license=('MIT')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=install
changelog=
source=(https://github.com/Microsoft/team-explorer-everywhere/releases/download/${pkgver}/TEE-CLC-${pkgver}.zip)
sha256sums=('54a3c868ac57304e88e60d5d86a7363d913582b4527af8daa7e60515721894bd')

package() {
  cd "$srcdir/TEE-CLC-$pkgver"
  mkdir -p ${pkgdir}/opt/tee-clc-${pkgver}
  cp -R help lib tf tf.cmd ${pkgdir}/opt/tee-clc-${pkgver}
  mkdir -p ${pkgdir}/usr/share/licenses/tee-clc/
  cp -R license.html ${pkgdir}/usr/share/licenses/tee-clc/
  mkdir -p ${pkgdir}/opt/tee-clc-${pkgver}/native/linux/
  if [ $(uname -m) == "i686" ] ; then
    cp -R native/linux/x86 ${pkgdir}/opt/tee-clc-${pkgver}/native/linux/
  else 
    cp -R native/linux/x86_64 ${pkgdir}/opt/tee-clc-${pkgver}/native/linux/
  fi
}
