pkgname=xfux
pkgver=2.1
pkgrel=2
pkgdesc="XFCE, but with animations and shadows. By OneDevelopment"
arch=('any')
depends=('xfce4-panel' 'xfce4-session' 'xfdesktop' 'picom-pijulius-git' 'python-pillow' 'tk')
url="https://github.com/OneDevelopmentPL/xfux"
# Pobieramy tylko pewne, lokalne pliki
source=('git+https://github.com/OneDevelopmentPL/xfux.git')
sha256sums=('SKIP')

package() {
  install -Dm755 "${srcdir}/xfux/xfux-session" "${pkgdir}/usr/bin/xfux-session"
  install -Dm755 "${srcdir}/xfux/xfux-splash" "${pkgdir}/usr/bin/xfux-splash"
  install -Dm644 "${srcdir}/xfux/xfux.desktop" "${pkgdir}/usr/share/xsessions/xfux.desktop"
  install -Dm644 "${srcdir}/xfux/xfux-logo.png" "${pkgdir}/usr/share/xfux/icons/xfux-logo.png"
  install -Dm644 "${srcdir}/xfux/xfux-wallpaper.png" "${pkgdir}/usr/share/xfux/backgrounds/xfux-wallpaper.png"
  install -Dm644 "${srcdir}/xfux/xfce4-panel.xml" "${pkgdir}/usr/share/xfux/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml"
  install -Dm644 "${srcdir}/xfux/xfce4-desktop.xml" "${pkgdir}/usr/share/xfux/xfce4/xfconf/xfce-perchannel-xml/xfce4-desktop.xml"
  install -Dm644 "${srcdir}/xfux/picom.conf" "${pkgdir}/usr/share/xfux/picom.conf"

}
