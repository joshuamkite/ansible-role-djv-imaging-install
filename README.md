joshuamkite.djv_imaging_install
=========

Role to install DJV Imaging as found at  http://djv.sourceforge.net/ but not made available as a PPA or 3rd party yum repo.

'DJV Imaging provides professional movie playback software for use in film, VFX, and computer animation.'

Supports (and tested on):

CentOS 7 (and probably 6)
RHEL 7 (and probably 6)
Ubuntu 16.04; 16:10; (and probably 17.04 onward)

For Ubuntu 

The deb available via Sourceforge from the project page has an undeclared dependency on libpng12 but this is not available from the repos for Ubuntu 16.10 onward, so the last distro packaged deb (for 16.04) is included

For RHEL/CentOS 

The rpm available via Sourceforge from the project page will not install on either CentOS 7 or RHEL 7 due package conflicts, as described at https://sourceforge.net/p/djv/bugs/47/ The repackaged rpm from that thread (http://leskinen.ru/files/djv-1.1-0.x86_64.rpm) is included here. As with Ubuntu there is an undeclared dependency on libpng12 but this is available via the standard repos and so it is installed from there. 

Requirements
------------

None

Role Variables
--------------

None

Dependencies
------------

x86_64 / AMD64 only

Example Playbook
----------------

---

    - hosts: servers
      roles:
         - joshuamkite.djv_imaging_install

License
-------

GPL v3

Author Information
------------------

joshuamkite@gmail.com
