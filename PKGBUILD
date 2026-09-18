# Maintainer: Abhimanyu Bhadauriya <abhimanyu@archlinux.org>
pkgname=iso2chd
pkgver=2.0.0
pkgrel=1
pkgdesc="Advanced batch ISO/BIN to CHD conversion utility by Abhimanyu Bhadauriya"
arch=('any')
url="https://github.com/penguin-crate/iso2chd"
license=('GPL-3.0-or-later')
depends=('bash' 'mame-tools' 'coreutils' 'gawk')
source=("iso2chd"
        "iso2chd.1")
sha256sums=('SKIP'
            'SKIP')

package() {
    install -Dm755 "$srcdir/iso2chd" "$pkgdir/usr/bin/iso2chd"
    install -Dm644 "$srcdir/iso2chd.1" "$pkgdir/usr/share/man/man1/iso2chd.1"
}
