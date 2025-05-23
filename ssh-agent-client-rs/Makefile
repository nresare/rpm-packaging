# whenever this is changed, the checksum file needs to be updated
version = 1.0.0

ssh-agent-client-rs-$(version).crate:
	curl -LO https://static.crates.io/crates/ssh-agent-client-rs/ssh-agent-client-rs-$(version).crate
	sha256sum -c ssh-agent-client-rs-1.0.0.crate.sha256

rust-ssh-agent-client-rs.spec: /usr/bin/rust2rpm
	rust2rpm ssh-agent-client-rs@$(version)

srpm: ssh-agent-client-rs-$(version).crate rust-ssh-agent-client-rs.spec
	rpmbuild -bs $(spec) --define "_sourcedir ." --define "_srcrpmdir $(outdir)"
