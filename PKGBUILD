pkgname=wiliwili-bin
pkgver=0.6.0
pkgrel=1
pkgdesc="一个专为手柄用户设计的第三方 B站客户端"
arch=('x86_64')
url="https://github.com/xfangfang/wiliwili"
license="GPL3"
depends=('mpv')
conflicts="wiliwili-git"
source=("https://gitee.com/hellopoisonx/aur-wiliwili-bin/raw/master/wiliwili", "https://gitee.com/hellopoisonx/aur-wiliwili-bin/raw/master/wiliwili.desktop")

package() {
  cd ${srcdir}
  #install the binary file
  install -Dm755 "wiliwili" "${pkgdir}/usr/bin/wiliwili"
  #Desktop file
  install -Dm755 "wiliwili.desktop" -t "$pkgdir/usr/share/applications/wiliwili.desktop" 
}
