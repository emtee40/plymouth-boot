systemd_unit_templates =                                                     \
        plymouth-start.service.in                                            \
        plymouth-read-write.service.in                                       \
        plymouth-quit.service.in                                             \
        plymouth-quit-wait.service.in                                        \
        plymouth-reboot.service.in                                           \
        plymouth-kexec.service.in                                            \
        plymouth-poweroff.service.in                                         \
        plymouth-halt.service.in

if ENABLE_SYSTEMD_INTEGRATION
systemdunitdir=$(SYSTEMD_UNIT_DIR)
systemdunit_DATA = $(systemd_unit_templates:.service.in=.service)
endif

EXTRA_DIST = $(systemd_unit_templates) $(systemdunit_DATA)
DISTCLEANFILES=$(systemdunit_DATA)