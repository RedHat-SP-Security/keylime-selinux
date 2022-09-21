## Keylime selinux-policy

This is upstream selinux policy for keylime.

## What is SELinux policy?

An SELinux policy describes the access permissions for all users, programs, processes, and files, and for the devices upon which they act. You can configure SELinux to implement either Targeted Policy or MultilevelSecurity (MLS) Policy. [1]

### What is keylime?

Keylime is an open-source scalable trust system harnessing TPM Technology. [2]

### How to apply keylime SELinux policy on the system manually?

```
dnf install selinux-policy-devel
git clone https://github.com/RedHat-SP-Security/keylime-selinux.git
cd keylime-selinux
make -f /usr/share/selinux/devel/Makefile keylime.pp
semodule -i keylime.pp
restorecon -R /
```

[1] https://web.mit.edu/rhel-doc/5/RHEL-5-manual/Deployment_Guide-en-US/rhlcommon-chapter-0001.html
[2] https://github.com/keylime/keylime/blob/master/README.md
