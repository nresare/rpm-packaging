/usr/bin/rust2rpm:
	dnf install -y rust2rpm rust2rpm-helper

srpm: /usr/bin/rust2rpm
	make -C $(shell dirname $(spec)) srpm
