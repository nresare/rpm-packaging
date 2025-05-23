ssh-agent-client-rs-1.0.0.crate:
	curl -LO https://static.crates.io/crates/ssh-agent-client-rs/ssh-agent-client-rs-1.0.0.crate
	sha256sum -c ssh-agent-client-rs-1.0.0.crate.sha256

srpm: ssh-agent-client-rs-1.0.0.crate
	rpmbuild -bs $(spec) --define "_sourcedir ." --define "_srcrpmdir $(outdir)"
