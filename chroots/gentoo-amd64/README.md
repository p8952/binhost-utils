Extract Gentoo stage3 files here:

	wget http://distfiles.gentoo.org/releases/amd64/autobuilds/$(curl -s http://distfiles.gentoo.org/releases/amd64/autobuilds/latest-stage3-amd64.txt | tail -n 1)^
	tar xvjpf stage3-*.tar.bz2
