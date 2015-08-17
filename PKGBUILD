# Maintainer: Huguenin Loïs <huguenindl at gmail dot com>
pkgname=oqapy
pkgver=1.9.1
pkgrel=1
pkgdesc="An application intended to sort files of the image type in graphic mode."
arch=('i686' 'x86_64')
url="http://www.oqapy.eu/"
    license=('GPL')
groups=()
    install='.install'
    depends=('python2>2.7' 'python2-pyqt>=4.5' 'pyexiv2>=0.2' 'gphoto2' 'dcraw' 'python2-imaging')
    source=(https://launchpad.net/oqapy/trunk/oqapy/+download/$pkgname-$pkgver.tar.gz)
md5sums=('292b05d2936c86422b9e88eb9ef0c060')

#generate with 'makepkg -g'

#build() {
#   }

    package() {
	cd "$srcdir/$pkgname-$pkgver"
	    mkdir -p $pkgdir/usr/share/$pkgname/
	    mkdir -p $pkgdir/usr/share/doc/$pkgname/
	    mkdir -p $pkgdir/usr/bin/
	    mkdir -p $pkgdir/usr/share/applications/
	    mkdir -p $pkgdir/usr/share/man/man1/
	    mkdir -p $pkgdir/usr/
	    cp *.py *.png $pkgdir/usr/share/$pkgname/
	    cp *.desktop $pkgdir/usr/share/applications/
	    cp oqapy.1 $pkgdir/usr/share/man/man1
	    cp -r doc/ $pkgdir/usr/share/doc/$pkgname/
	    cp -r medias/ $pkgdir/usr/share/$pkgname/
	    cp -r configPages/ $pkgdir/usr/share/$pkgname/
	    cp -r VWidgets/ $pkgdir/usr/share/$pkgname/
	    cp -r camerahandler $pkgdir/usr/share/$pkgname/
	    cp -r g9n/ $pkgdir/usr/share/$pkgname/
	    cp -r printing/ $pkgdir/usr/share/$pkgname/
	    cp -r commonwidgets $pkgdir/usr/share/$pkgname/
	    cp -r locale/ $pkgdir/usr/
	    cp $pkgname $pkgdir/usr/bin/
	    sed -i -e "s|#![ ]*/usr/bin/python$|#!/usr/bin/python2|" \
	    -e "s|#![ ]*/usr/bin/env python$|#!/usr/bin/env python2|" \
	    -e "s|\"python\"|\"python2\"|" \
	    $(find $pkgdir -name "$pkgname.py" -or -name "$pkgname" -and -perm -o+rx -type f)
    }

