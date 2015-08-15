# Maintainer: Xu Fasheng <fasheng.xu[AT]gmail.com>
# Contributor: Josip Ponjavic <josipponjavic at gmail dot com>

pkgname=deepin-icon-theme
pkgver=git20140506153346
pkgrel=1
pkgdesc='Icon theme from Linux Deepin'
arch=('any')
url="http://www.linuxdeepin.com/"
license=('LGPL3')
depends=('faenza-icon-theme')

_fileurl=http://packages.linuxdeepin.com/deepin/pool/main/d/deepin-icon-theme/deepin-icon-theme_13.06.12+git20140506153346~36977ed295~2014.tar.gz
source=("${_fileurl}")
md5sums=('47706ce3038009075a4488ef7055074c')

_filename="$(basename "${_fileurl}")"
_filename="${_filename%.tar.gz}"
_innerdir="${_filename/_/-}"

_install_copyright_and_changelog() {
    mkdir -p "${pkgdir}/usr/share/doc/${pkgname}"
    cp -f debian/copyright "${pkgdir}/usr/share/doc/${pkgname}/"
    gzip -c debian/changelog > "${pkgdir}/usr/share/doc/${pkgname}/changelog.gz"
}

package() {
    cd "${srcdir}/${_innerdir}"

    mkdir -p "$pkgdir/usr/share/icons"
    cp -rf Deepin "$pkgdir/usr/share/icons/"
    cp -rf Deepin-blue "$pkgdir/usr/share/icons/"
    # cp -rf Deepin-sapphire "$pkgdir/usr/share/icons/Deepin"

    _install_copyright_and_changelog
}
