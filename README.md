# CJIS_sandbox

fedora-31
~~~~
[vagrant@srvstack-01 ~]$ sudo ansible-galaxy install RedHatOfficial.rhel8_cjis
[vagrant@srvstack-01 ~]$ sudo ansible-playbook -i "localhost," -c local --check /vagrant/playbook.yml

TASK [RedHatOfficial.rhel8_cjis : Read signatures in GPG key] *******************************************************************************************************************************
fatal: [localhost]: FAILED! => {"changed": false, "cmd": "set -o pipefail\ngpg --show-keys --with-fingerprint --with-colons \"/etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release\" | grep -A1 \"^pub\" | grep \"^fpr\" | cut -d \":\" -f 10\n", "delta": "0:00:00.322988", "end": "2020-02-17 14:59:02.788414", "msg": "non-zero return code", "rc": 1, "start": "2020-02-17 14:59:02.465426", "stderr": "gpg: directory '/root/.gnupg' created\ngpg: keybox '/root/.gnupg/pubring.kbx' created\ngpg: can't open '/etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release': No such file or directory", "stderr_lines": ["gpg: directory '/root/.gnupg' created", "gpg: keybox '/root/.gnupg/pubring.kbx' created", "gpg: can't open '/etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release': No such file or directory"], "stdout": "", "stdout_lines": []}

PLAY RECAP **********************************************************************************************************************************************************************************
localhost                  : ok=23   changed=11   unreachable=0    failed=1    skipped=2    rescued=0    ignored=0

~~~~
centos-8.0
~~~~
sudo required

[vagrant@srvstack-02 ~]$ sudo ansible-galaxy install RedHatOfficial.rhel8_cjis
[vagrant@srvstack-02 ~]$ sudo ansible-playbook -i "localhost," -c local --check /vagrant/playbook.yml

TASK [RedHatOfficial.rhel8_cjis : Read signatures in GPG key] *******************************************************************************************************************************
fatal: [localhost]: FAILED! => {"changed": false, "cmd": "set -o pipefail\ngpg --show-keys --with-fingerprint --with-colons \"/etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release\" | grep -A1 \"^pub\" | grep \"^fpr\" | cut -d \":\" -f 10\n", "delta": "0:00:00.074890", "end": "2020-02-17 14:42:27.320111", "msg": "non-zero return code", "rc": 1, "start": "2020-02-17 14:42:27.245221", "stderr": "gpg: directory '/root/.gnupg' created\ngpg: keybox '/root/.gnupg/pubring.kbx' created\ngpg: can't open '/etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release': No such file or directory", "stderr_lines": ["gpg: directory '/root/.gnupg' created", "gpg: keybox '/root/.gnupg/pubring.kbx' created", "gpg: can't open '/etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release': No such file or directory"], "stdout": "", "stdout_lines": []}

PLAY RECAP **********************************************************************************************************************************************************************************
localhost                  : ok=22   changed=13   unreachable=0    failed=1    skipped=3    rescued=0    ignored=0
~~~~
~~~~


Criminal Justice Information Services (CJIS) Security Policy
https://github.com/RedHatOfficial/ansible-role-rhel8-cjis

CCE-80872-5
CCE-80872-5 	Enable auditd Service
http://people.redhat.com/swells/table-rhel8-cces.html

Guide to the Secure Configuration of Red Hat Enterprise Linux 8
http://static.open-scap.org/ssg-guides/ssg-rhel8-guide-cui.html

 NIST-800-53-AC-2(g)
 g. Monitors the use of information system accounts;
 https://nvd.nist.gov/800-53/Rev4/control/AC-2

 NIST-800-53-AU-3
 AU-3 CONTENT OF AUDIT RECORDS
 https://nvd.nist.gov/800-53/Rev4/control/AU-3#enhancement-1

 PCI-DSS-Req-10.2.2
 10.2.2 All actions taken by any individual with root or administrative privileges.
 http://pcidsscompliance.net/pci-dss-requirements/how-to-comply-to-requirement-10-of-pci-dss/

 CJIS Security Policy Resource Center
 https://www.fbi.gov/services/cjis/cjis-security-policy-resource-center

 Guide to the Secure Configuration of Red Hat Enterprise Linux 8
 http://static.open-scap.org/ssg-guides/ssg-rhel8-guide-cui.html
~~~~
