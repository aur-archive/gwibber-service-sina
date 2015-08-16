# Contributor: skatiger <skatiger at gmail dot com>

pkgname=gwibber-service-sina
pkgver=0.9.1
pkgrel=4
pkgdesc='sina weibo service for gwibber'
arch=('i686' 'x86_64')
url='http://launchpad.net/gwibber-service-sina'
license=('GPL2')
depends=('gwibber>=3.3.90' 'python2>=2.7')
makedepends=('python2-distutils-extra')

source=("http://launchpad.net/gwibber-service-sina/trunk/${pkgver}/+download/gwibber-service-sina-${pkgver}.tar.gz"
       'sina'
       'gwibber-3.3.90-sina.patch')

build()
{
	cd "$srcdir/${pkgname}-$pkgver"
    patch -p0 <../gwibber-3.3.90-sina.patch
    python2 setup.py install --root="${pkgdir}"

    # Add OAUTH file
    cp ../sina ${pkgdir}/usr/share/gwibber/plugins/sina/data/
}
md5sums=('3d6ea761e91baf1a206c3ce8bc85da24'
         'd0adf30bebcdedf09de1b02799a85a8d'
         '3edbd4d6b7753b3baa62dedb97dfcf35')
