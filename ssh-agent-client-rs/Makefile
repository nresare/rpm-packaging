# whenever this is changed, the checksum file needs to be updated
version = 1.0.0
crate = ssh-agent-client-rs

$(crate)-$(version).crate:
	curl -LO https://static.crates.io/crates/$(crate)/$(crate)-$(version).crate
	sha256sum -c crate.sha256

rust-$(crate).spec: /usr/bin/rust2rpm
	rust2rpm $(crate)@$(version)

srpm: $(crate)-$(version).crate rust-$(crate).spec
	rpmbuild -bs $(spec) --define "_sourcedir ." --define "_srcrpmdir $(outdir)"
