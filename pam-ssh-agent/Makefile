pam-ssh-agent-0.9.0.crate:
	curl -LO https://static.crates.io/crates/pam-ssh-agent/pam-ssh-agent-0.9.0.crate
	sha256sum -c pam-ssh-agent-0.9.0.crate.sha256

rust-pam-ssh-agent.spec:
	rust2rpm pam-ssh-agent

srpm: pam-ssh-agent-0.9.0.crate rust-pam-ssh-agent.spec
	rpmbuild -bs $(spec) --define "_sourcedir ." --define "_srcrpmdir $(outdir)"
