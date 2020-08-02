pkgname=device-xiaomi-mido-mainline
pkgdesc="Xiaomi Redmi Note 4X"
pkgver=1.0
pkgrel=0
url="https://postmarketos.org"
license="MIT"
arch="aarch64"
options="!check !archcheck"
depends="postmarketos-base mkbootimg soc-qcom-msm8916 linux-postmarketos-qcom-msm8953"
makedepends="devicepkg-dev"
source="deviceinfo"
subpackages="
	$pkgname-nonfree-firmware:nonfree_firmware
"
build() {
	devicepkg_build $startdir $pkgname
}

package() {
	devicepkg_package $startdir $pkgname
}

nonfree_firmware() {
	pkgdesc="Proprietary firmware"
	depends="linux-firmware-qcom firmware-xiaomi-mido-mainline"
	mkdir "$subpkgdir"
}

