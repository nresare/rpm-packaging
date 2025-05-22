srpm:
        # For this to work for the general case, set spec to the name of the specfile and subdirectory to the relevant subdir
        # in the copr ui for the package
	cd $(shell dirname $(spec)) && \
	rpmbuild -bs --undefine=_disable_source_fetch $(spec) --define "_sourcedir ." --define "_srcrpmdir $(outdir)"
