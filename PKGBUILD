pkgname=xfux
pkgver=2.1
pkgrel=2
pkgdesc="XFCE, but with animations and shadows. By OneDevelopment"
arch=('any')
depends=('xfce4-panel' 'xfce4-session' 'xfdesktop' 'picom-pijulius-git' 'python-pillow' 'tk')

# Pobieramy tylko pewne, lokalne pliki
source=('xfux.desktop'
        'xfux-logo.png'
        'xfux-session'
        'xfce4-panel-style.tar.bz2'
        'xfce4-desktop.xml'
        'xfux-wallpaper.png'
        'picom.conf'
        'xfux-splash')

sha256sums=('SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP')

package() {
  # 1. Skrypty i sesja
  install -Dm755 "${srcdir}/xfux-session" "${pkgdir}/usr/bin/xfux-session"
  install -Dm755 "${srcdir}/xfux-splash" "${pkgdir}/usr/bin/xfux-splash"
  install -Dm644 "${srcdir}/xfux.desktop" "${pkgdir}/usr/share/xsessions/xfux.desktop"

  # 2. Grafika
  install -Dm644 "${srcdir}/xfux-logo.png" "${pkgdir}/usr/share/pixmaps/xfux-logo.png"
  install -Dm644 "${srcdir}/xfux-wallpaper.png" "${pkgdir}/usr/share/backgrounds/xfux/xfux-wallpaper.png"

  # 3. Pliki konfiguracyjne
  install -Dm644 "${srcdir}/xfce4-panel.xml" "${pkgdir}/usr/share/xfux/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml"
  install -Dm644 "${srcdir}/xfce4-desktop.xml" "${pkgdir}/usr/share/xfux/xfce4/xfconf/xfce-perchannel-xml/xfce4-desktop.xml"
  install -Dm644 "${srcdir}/picom.conf" "${pkgdir}/usr/share/xfux/picom.conf"
}
