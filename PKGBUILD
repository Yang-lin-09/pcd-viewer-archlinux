# Maintainer: Lucky
# Contributor: tewi_r <https://github.com/7ew1r>

pkgname=pcd-viewer
pkgver=0.1
pkgrel=1
pkgdesc="A simple PCD (Point Cloud Data) file viewer for archlinux"
arch=('x86_64' 'i686')
license=('MIT')
depends=('glfw' 'pcl')
source=("git+https://github.com/Yang-lin-09/pcd-viewer.git")

sha256sums=('SKIP')

build() {
 # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  cmake ${srcdir}/pcd-viewer/
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR=${pkgdir} install

  install -Dm644 ${srcdir}/pcd-viewer/LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
