# Maintainer: Fancy Zhang <springzfx@gmail.com>
# pkgbase=ap
pkgname=ap
pkgver=1.0
pkgrel=1
pkgdesc="simple wireless ap support both ipv4 and ipv6 with nat"
arch=('x86_64')
url="https://github.com/springzfx/ap"
license=('GPL')
depends=('hostapd'  'dnsmasq')
optdepends=('systemd: for service')

source_x86_64=(
"ap.sh"
"ap.conf"
"ap.service"
"dnsmasq-template.sh"
"hostapd-template.sh"
"iptables-add.sh"
"iptables-del.sh"
"ap.resume"
)
md5sums_x86_64=('a9c8310e97f068e0fda2bc344e193bf6'
                '0c32f6a1247fbed359b49af3378864bf'
                '8244fa16d1aa23ac7d5de8eadc0bfdf1'
                'ec1aa2a300f5b389685a3c2ad2cb2044'
                '8a037211128d2cccb543608f77838f50'
                'aec42e1591ca85c48823b41e2ab59bbb'
                'aed4844517ddcbadd357441242840225'
                '62d9b8c46bc405e96f71925544292aa9')

backup=('etc/ap/ap.conf')

package_ap(){
    install -d ${pkgdir}/usr/lib/systemd/system/ ${pkgdir}/etc/ap/ ${pkgdir}/usr/share/ap/ ${pkgdir}/usr/bin/ \
               ${pkgdir}/usr/lib/systemd/system-sleep/
    install -m 444 ap.service ${pkgdir}/usr/lib/systemd/system/
    install -m 544 ap.sh ${pkgdir}/usr/bin/ap
    install -m 644 ap.conf ${pkgdir}/etc/ap/
    install -m 444 iptables-add.sh iptables-del.sh dnsmasq-template.sh hostapd-template.sh ${pkgdir}/usr/share/ap/
    install -m 544 ap.resume ${pkgdir}/usr/lib/systemd/system-sleep/
}
