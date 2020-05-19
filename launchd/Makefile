.PHONY: install uninstall

PREFIX = /usr/local
LAUNCHD_DIR = /Library
LAUNCHD_DAEMON_DIR = $(LAUNCHD_DIR)/LaunchDaemons

install:
	sed "s|@PREFIX@|$(PREFIX)|" in.biscuitt.popub-local.plist.in > in.biscuitt.popub-local.plist
	sed "s|@PREFIX@|$(PREFIX)|" in.biscuitt.popub-relay.plist.in > in.biscuitt.popub-relay.plist
	install -m0644 in.biscuitt.popub-local.plist "$(DESTDIR)$(LAUNCHD_DAEMON_DIR)/in.biscuitt.popub-local.plist"
	install -m0644 in.biscuitt.popub-relay.plist "$(DESTDIR)$(LAUNCHD_DAEMON_DIR)/in.biscuitt.popub-relay.plist"

uninstall:
	rm -f "$(DESTDIR)$(LAUNCHD_DAEMON_DIR)"/in.biscuitt.popub-{local,relay}.plist
