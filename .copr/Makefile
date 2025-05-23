/usr/bin/rust2rpm:
        dnf install -y rust2rpm

srpm: /usr/bin/rust2rpm
	make -C $(shell dirname $(spec)) srpm
