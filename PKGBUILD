pkgname=wiliwili-bin
pkgver=0.6.0
pkgrel=1
pkgdesc="一个专为手柄用户设计的第三方 B站客户端"
arch=('x86_64')
url="https://github.com/xfangfang/wiliwili"
license=("GPL3")
depends=('mpv')
conflicts=("wiliwili-git")
source=("https://gitee.com/hellopoisonx/aur-wiliwili-bin/raw/master/wiliwili.tar.gz" "https://gitee.com/hellopoisonx/aur-wiliwili-bin/raw/master/wiliwili.desktop" "https://gitee.com/hellopoisonx/aur-wiliwili-bin/raw/master/resources.tar.gz")
sha256sums=('3684c3158caba48d2047d1983530fb1f3a940b37dce7e735d460d582cd860590'
            '63fe4482e054d670450d27a9928c7f5682d6975370e629583ba6d279798f6303'
            '4bfcf70e927004d47a567e1e6b13fda2e8104f8cedbe0a83694971a4537519b8')
prepare() {
  cd ${srcdir}
  tar xpvf wiliwili.tar.gz -C "$srcdir"
  tar xpvf resources.tar.gz -C "$srcdir"
}

package() {
  cd ${srcdir}
  mkdir -p "${pkgdir}/usr/share/wiliwili"
  #resources
  cp -r  "${srcdir}/resources" "${pkgdir}/usr/share/wiliwili/"
  #install the binary file
  install -Dm755 "wiliwili" "${pkgdir}/usr/bin/wiliwili"
  #Desktop file
  install -Dm755 "wiliwili.desktop" -t "$pkgdir/usr/share/applications/wiliwili.desktop" 
}
