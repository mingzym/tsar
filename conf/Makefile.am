AUTOMAKE_OPTIONS = foreign

confdir=/etc/tsar
conf_DATA= nagios.conf tsar.conf
confddir=/etc/tsar/conf.d
confd_DATA=
rotatedir=/etc/logrotate.d
mandir=${datadir}/man

rotate_DATA=tsar.logrotate

crondir=/etc/cron.d
cron_DATA=tsar_cron

tsar_cron:
	echo '# tsar collect data every minute' > tsar_cron
	echo 'MAILTO=""' >> tsar_cron
	echo '* * * * * root '"${bindir}"'/tsar --cron > /dev/null 2>&1' >> tsar_cron

EXTRA_DIST=$(conf_DATA) $(rotate_DATA) tsar.8 $(cron_DATA)

man_MANS=tsar.8
clean-local:
	rm -f tsar_cron
