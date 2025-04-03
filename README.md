# Unofficial Debian Mail-in-a-Box

=============

Simple porting of Mailinabox to Debian 12.
Original project: [https://github.com/mailinabox/mailinabox](https://github.com/mail-in-a-box/mailinabox)

## Version

Current version: v67.2.0-AiutoPcAmico
Upstream current implemented version: v67

## Changes implemented

- Compatibility with Debian 12.
- Updated php to version 8.2
- At the moment, OwnCloud is disabled, because it not supports php8.2
- Changed SMTP server sign
- more restrictive Fail2Ban configuration
- ask the user if he wants to disable the graylist

## Future implementation

- Changing the default index page more easily

## broken functionality

- Duplicity (At the moment, I don't understand why the /etc/duplicity folder is not generated)
- OwnCloud

## Installation guide

Please, open the file "INSTALL.md" for the complete guide to install Debian Mail-in-a-Box by AiutoPcAmico

## Changelogs

- SMTP ([postfix](http://www.postfix.org/)), IMAP ([Dovecot](http://dovecot.org/)), CardDAV/CalDAV ([Nextcloud](https://nextcloud.com/)), and Exchange ActiveSync ([z-push](http://z-push.org/)) servers
- Webmail ([Roundcube](http://roundcube.net/)), mail filter rules (thanks to Roundcube and Dovecot), and email client autoconfig settings (served by [nginx](http://nginx.org/))
- Spam filtering ([spamassassin](https://spamassassin.apache.org/)) and greylisting ([postgrey](http://postgrey.schweikert.ch/))
- DNS ([nsd4](https://www.nlnetlabs.nl/projects/nsd/)) with [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework), DKIM ([OpenDKIM](http://www.opendkim.org/)), [DMARC](https://en.wikipedia.org/wiki/DMARC), [DNSSEC](https://en.wikipedia.org/wiki/DNSSEC), [DANE TLSA](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities), [MTA-STS](https://tools.ietf.org/html/rfc8461), and [SSHFP](https://tools.ietf.org/html/rfc4255) policy records automatically set
- TLS certificates are automatically provisioned using [Let's Encrypt](https://letsencrypt.org/) for protecting https and all of the other services on the box
- Backups ([duplicity](http://duplicity.nongnu.org/)), firewall ([ufw](https://launchpad.net/ufw)), intrusion protection ([fail2ban](http://www.fail2ban.org/wiki/index.php/Main_Page)), and basic system monitoring ([munin](http://munin-monitoring.org/))

- CHANGELOG.md is from the upstream project
- CHANGELOG_AiutoPcAmico.md relates to the changes made by AiutoPcAmico and strictly connected to the Debian porting
