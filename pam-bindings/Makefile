# whenever this is changed, the checksum file needs to be updated
version = 0.1.1
crate = pam-bindings

rust-pam-bindings.spec:
	rust2rpm --ignore-missing-license-files $(crate)@$(version)

$(crate)-$(version).crate:
	curl -LO https://static.crates.io/crates/$(crate)/$(crate)-$(version).crate
	sha256sum -c crate.sha256

srpm: $(crate)-$(version).crate
	rpmbuild -bs $(spec) --define "_sourcedir ." --define "_srcrpmdir $(outdir)"
