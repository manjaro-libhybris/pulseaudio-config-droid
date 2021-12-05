# Contributor: Erik Inkinen <erik.inkinen@gmail.com>

pkgname=pulseaudio-config-droid
provides=('pulseaudio-config-droid')
pkgver=0.1
pkgrel=1
pkgdesc="Pulseaudio configuration for Halium"
arch=('any')
url="https://github.com/manjaro-libhybris/pulseaudio-config-droid"
license=('GPL2')
depends=('pulseaudio')
makedepends=('git')
source=('pulseaudio-config-droid::git+https://github.com/manjaro-libhybris/pulseaudio-config-droid.git')
md5sums=('SKIP')

package() {
    cd pulseaudio-config-droid

    install -d ${pkgdir}/etc/pulse
    install -m 644 pulse/droid.pa ${pkgdir}/etc/pulse/
    install -m 644 pulse/touch-stream-restore.table ${pkgdir}/etc/pulse/

    install -d ${pkgdir}/etc/systemd/user/pulseaudio.service.d
    install -m 644 pulseaudio.service.d/10-lxc-android.conf ${pkgdir}/etc/systemd/user/pulseaudio.service.d
    install -m 644 pulseaudio.service.d/20-droid-wait.conf ${pkgdir}/etc/systemd/user/pulseaudio.service.d
    install -m 644 pulseaudio.service.d/30-droid-config.conf ${pkgdir}/etc/systemd/user/pulseaudio.service.d
}

