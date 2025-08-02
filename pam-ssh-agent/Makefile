# whenever this is changed, the checksum file needs to be updated
version = 0.9.2

pam-ssh-agent-$(version).crate:
	curl -LO https://static.crates.io/crates/pam-ssh-agent/pam-ssh-agent-$(version).crate
	sha256sum -c crate.sha256

rust-pam-ssh-agent.spec: /usr/bin/rust2rpm
	rust2rpm pam-ssh-agent@$(version)

srpm: pam-ssh-agent-$(version).crate rust-pam-ssh-agent.spec
	rpmbuild -bs $(spec) --define "_sourcedir ." --define "_srcrpmdir $(outdir)"
