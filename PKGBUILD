# Maintainer: xVan Turing <xVanTuring@outlook.com> 

pkgname=substance-designer
pkgver=10.1.3
pkgrel=1
_build=3687
install='substance-designer.install'
pkgdesc="Node-based, non-destructive PBR material authoring tool."
arch=('x86_64')
url='https://www.allegorithmic.com/products/substance-designer'
license=('custom')
depends=('fontconfig' 'gcc-libs-multilib' 'glu' 'hicolor-icon-theme' 'libtiff4')
options=('!strip')
source=("https://download.substance3d.com/substance-designer/10.x/Substance_Designer-${pkgver}-${_build}-linux-x64-standard.rpm"
        'mime.patch'
        'desktop.patch')
noextract=()
sha256sums=('2457481fa406dfaffb433d713e3cd6c3fe6c5d38015f4631ae99c923ed23818f'
            'b40eb42e4181667da77dde323fa80032203c73746d675f2a011606dca9887324'
            'e9ae7c758bb2837b56704b31842289b5b1cb8c50481258ce61fd22a1583f1b6e')
validpgpkeys=()
prepare(){
  patch ${srcdir}/opt/Allegorithmic/Substance_Designer/resources/allegorithmic-x.allegorithmic.xml ${srcdir}/mime.patch
  patch ${srcdir}/opt/Allegorithmic/Substance_Designer/resources/allegorithmic-Substance_Designer.desktop ${srcdir}/desktop.patch
}
package() {
  mkdir -p ${pkgdir}/opt/Allegorithmic
  mv ${srcdir}/opt/Allegorithmic/Substance_Designer ${pkgdir}/opt/Allegorithmic
}
