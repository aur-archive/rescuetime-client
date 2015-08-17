pkgname=rescuetime-client
pkgver=99
pkgrel=0
pkgdesc="rescuetime linux client"
url="https://launchpad.net/rescuetime-linux-uploader"
depends=('python' 'setuptools' 'xorg-utils')
license=('MIT')
arch=(any)
conflicts=('rescuetime')
source=("http://launchpad.net/rescuetime-linux-uploader/trunk/$pkgver/+download/rescuetime-linux-uploader-$pkgver.tar.bz2")
md5sums=('e16d03a34498990bf8adf2fcbebcbee8')

build() {
	cd $srcdir/rescuetime-linux-uploader-$pkgver
	python setup.py build
	python setup.py install --prefix=/usr --root="$pkgdir" || return 1
	install -D gnome_applet/rescuetime_16.png $pkgdir/usr/share/icons/hicolor/16x16/rescuetime.png
	install -D gnome_applet/rescuetime_22.png $pkgdir/usr/share/icons/hicolor/22x22/rescuetime.png
	install -D gnome_applet/rescuetime_32.png $pkgdir/usr/share/icons/hicolor/32x32/rescuetime.png
	install -D gnome_applet/rescuetime_48.png $pkgdir/usr/share/icons/hicolor/48x48/rescuetime.png
	install -D gnome_applet/rescuetime_48.png $pkgdir/usr/share/pixmaps/rescuetime.png
	install -D gnome_applet/rescuetime_tracker.server $pkgdir/usr/lib/bonobo/servers/rescuetime_tracker.server
	install -D gnome_applet/rescuetime_notifier.server $pkgdir/usr/lib/bonobo/servers/rescuetime_notifier.server
}
