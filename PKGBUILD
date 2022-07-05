pkgname=secure-boot-kit
pkgver=1.0
pkgrel=1
pkgdesc="setup secure boot with shim and systemd-boot"
arch=('x86_64')
url="https://github.com/kimotu4632uz/secure-boot-kit"
license=('GPL')
depends=('shim-signed' 'systemd' 'pacman')
conflicts=()
replaces=()
backup=()
install=systemd-setup.install
source=("99-secureboot-kernel.hook"
        "99-shim-update.hook"
        "systemd-boot-secureboot.service")

sha256sums=('031672c56a3cf4dee08c7ed1a1bbdfd8f490b234be7b63e45fb4b1ce191217aa'
            '263e9564a47b27fe81fa91f1d1118e68a7183af9477c85bee15f7575da2e0707'
            '918ac1bdc9a8293b681c8e813f4bfacac79384bcb33ee4ede905c434efabd986')

prepare() {
  :
}

build() {
  :
}

package() {
  install -Dm644 -t "$pkgdir/etc/pacman.d/hooks/" 99-secureboot-kernel.hook
  install -Dm644 -t "$pkgdir/etc/pacman.d/hooks/" 99-shim-update.hook
  install -Dm644 -t "$pkgdir/usr/lib/systemd/system/" systemd-boot-secureboot.service
}
