pam-bindings-0.1.1.crate:
	curl -LO https://static.crates.io/crates/pam-bindings/pam-bindings-0.1.1.crate
	sha256sum -c pam-bindings-0.1.1.crate.sha256

srpm: pam-bindings-0.1.1.crate
	rpmbuild -bs $(spec) --define "_sourcedir ." --define "_srcrpmdir $(outdir)"
