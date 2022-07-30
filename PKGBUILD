# Maintainer: Jonathan < >

#pkgname=librescanner
pkgname=horus
pkgver=0.0.1
pkgrel=1
pkgdesc="Free scanner software for Ciclop Horus 3D scanner"
arch=('x86_64' 'i686' 'arm' 'armv6h' 'armv7h' 'aarch64')
url="https://github.com/bqlabs/horus"
#url="https://github.com/LibreScanner/horus"
#license=('AGPL3')
depends=('python' 'python-wxpython' 'python-pyserial' 'python-opengl' 'python-opencv'
         'python-pyglet' 'python-numpy' 'python-scipy' 'python-matplotlib'
         'v4l-utils' 'wxgtk3')
#python-queuelib
#opencv-python
#python-importlib_resources
optdepends=('avrdude: flash board firmware'
            'mjpg-streamer: stream images from webcam'
            'python-nose: debug')
provides=('horus')
conflicts=('horus')
#install=octoprint.install
source=("https://github.com/LibreScanner/horus/archive/refs/tags/0.2rc1.tar.gz")

sha256sums=('908ddd0a20e67d04854914a9cb09a0f3b9221ec1f1ee7f03d77934b4377d9952')

# horus release version:
_horusver=0.2rc1

prepare() {
    cd "${srcdir}"
    # backup files to prevert overwriting by makepkg:
#    cp -r ../pkg ../pkg_horus
}

package() {
    cd "${srcdir}/horus-${_horusver}"
    
#    #remove old files:
#    FILES=(LICENSE horus PKGBUILD setup.py package.sh test res doc setup_mac.py pkg README.md CHANGELOG)
#    rm -dr -f ${FILES}
    
#    #copy all files:
#    for f in "${FILES[@]}"; do
#      cp -r "../../${f}" ./;
#    done

#    mkdir ./pkg
#    cp -r ../../pkg_horus/* ./pkg

#    python3 -m venv "${pkgdir}/opt/$pkgname"

#    "${pkgdir}/opt/$pkgname/bin/pip3" install wheel
#    "${pkgdir}/opt/$pkgname/bin/pip3" install netifaces

#    "${pkgdir}/opt/$pkgname/bin/python3" setup.py install --optimize=1
#    sed -i "s|${pkgdir}/opt/$pkgname|/opt/$pkgname|g" "${pkgdir}/opt/$pkgname/bin/"* # relocate without breaking plugin system

#    install -Dm644 "${srcdir}/octoprint.service" "${pkgdir}/usr/lib/systemd/system/octoprint.service"
#    install -Dm644 "${srcdir}/octoprint.sysusers" "${pkgdir}/usr/lib/sysusers.d/octoprint.conf"
#    install -Dm644 "${srcdir}/octoprint.tmpfiles" "${pkgdir}/usr/lib/tmpfiles.d/octoprint.conf"

#     install -d "${pkgdir}/usr/bin/" ln -s /opt/$pkgname/bin/octoprint 
#     "${pkgdir}/usr/bin/octoprint"

#    install -d "${pkgdir}/var/lib/octoprint" "${pkgdir}/etc/"
#    ln -s /var/lib/octoprint/.octoprint/ "${pkgdir}/etc/octoprint"

    python setup.py install --root="$pkgdir"
}
