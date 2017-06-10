pkgname=tanks-of-freedom
pkgver=0.6.3
pkgrel=1
pkgdesc="A classic turn-based strategy game with two armies fighting against each other."
arch=('x86_64')
url="http://tof.p1x.in"
license=('MIT')
depends=('godot')
source=("https://github.com/w84death/Tanks-of-Freedom/archive/${pkgver}-beta.tar.gz"
        'tanks-of-freedom.desktop'
        'launch-tanks-of-freedom.sh')
md5sums=('9312c9ff9991dad725ec80b17bb76a31'
         '8b74235c963e4aab293bc334763ea851'
         'bb7ae1da8d6a254b928dc7d1de4e5799')

package() {
    cd Tanks-of-Freedom-${pkgver}-beta
    
    install -d ${pkgdir}/opt/${pkgname}
    cp -r * ${pkgdir}/opt/${pkgname}/
    chmod 755 -R ${pkgdir}/opt/${pkgname}
    
    install -Dm755 ${srcdir}/launch-${pkgname}.sh ${pkgdir}/usr/bin/launch-${pkgname}.sh
    install -Dm644 $srcdir/${pkgname}.desktop ${pkgdir}/usr/share/applications/${pkgname}.desktop
    install -Dm644 ${srcdir}/Tanks-of-Freedom-${pkgver}-beta/assets/icons/icon48.png ${pkgdir}/usr/share/pixmaps/${pkgname}.png
}
