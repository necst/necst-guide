.. -*- coding: utf-8 -*-

.. _facilities:

Facilities and Services: What's in the Lab
==========================================

The `NECSTLab`_ offers several facilities such as computing equipment, resources and services such as web hosting for small projects, management platforms, and code repositories.

Access to the facilities that require network connectivity is regulated by the :ref:`rules` and is granted once you obtain access to the lab (see :ref:`access`).

.. _access-facilities:

How to Obtain Access to the Computing Resources and Services
------------------------------------------------------------

Access to computing resources and services is regulated through individual accounts. To obtain an account, follow this procedure:

#. Obtain access to the lab (see :ref:`access`)
#. Send an email to `Federico Maggi`_ with the :ref:`radrl` in Cc: `fede@maggi.cc <mailto:fede@maggi.cc?subject=[NECSTLab]%20Network%20access%20request&amp;cc=marco.santambrogio@polimi.it>`_

Without an account, you are still allowed to connect to the local network via wired medium (see :ref:`lan`) and reach unauthenticated services and resources. However, most of the services and resources require authentication.

  .. warning::
     Please, do change your password!

.. _ssl:

SSL Security Warnings
~~~~~~~~~~~~~~~~~~~~~

Whenever you access a resource via SSL (e.g., :kbd:`https://...`), your client (e.g., browser, SVN client, Git client) will display a security warning that says that the SSL certificate is not trusted. This happens because such certificate is (self) signed by the lab's certification authority (CA), which itself is not trusted.

.. figure:: ../_static/images/ssl-warning.png
   :scale: 75 %
   :alt: SSL warning example

   SSL warning example.


.. figure:: ../_static/images/certificate-detail.png
   :scale: 75 %
   :alt: SSL certificate details

   SSL certificate details.

This is perfectly normal. If you are connecting from within the lab local network you can safely confirm the security exception.

However, accepting the security exception from outside the lab network may present some security issues. There are two solutions to this:

* from within the lab network, connect to the service that is raising such security exception and accept that certificate permanently.

* (safer) from within the lab network, download the CA certificate from the following URL and add it to the list of trusted CAs on your computer (a.k.a., keychain).

   https://home.necst.elet.polimi.it/cacert.pem

  which has the following fingerprints

  .. code-block:: none

     SHA1 BD 92 4F 1A B0 75 92 0C 76 0C CC B7 E4 65 AF B8 1C 66 C3 2E
      MD5 1C 45 E5 38 CA 0D BA D7 03 77 39 C9 1B 6D 5D 48

  alternatively, you can copy and paste the following PEM version of the certificate:

  .. code-block:: none

     -----BEGIN CERTIFICATE-----
     MIICvDCCAiWgAwIBAgIJAOxEbwAjWP1CMA0GCSqGSIb3DQEBBQUAMEkxGTAXBgNV
     BAoTEE5FQ1NUIExhYm9yYXRvcnkxLDAqBgNVBAMTI0NlcnRpZmljYXRpb24gQXV0
     aG9yaXR5IENlcnRpZmljYXRlMB4XDTEyMDMwODE0NDUwNVoXDTIyMDMwNjE0NDUw
     NVowSTEZMBcGA1UEChMQTkVDU1QgTGFib3JhdG9yeTEsMCoGA1UEAxMjQ2VydGlm
     aWNhdGlvbiBBdXRob3JpdHkgQ2VydGlmaWNhdGUwgZ8wDQYJKoZIhvcNAQEBBQAD
     gY0AMIGJAoGBALzFwbzJaqvTMrkyG23pGAxFe8ydRilg51T6Jzbk78N6O4/Rc5Do
     VLlRfu9gFcSc8KVYPiGRzfdAgQaOjl8V+zi2rQcdhxzRXtNF7bPLk/LLox6LDmbK
     OUoa+HvTE56AsMloW8Yfwz61nX7m+ySRRmNFjyoKcMzbAs4m5qVYLUE3AgMBAAGj
     gaswgagwHQYDVR0OBBYEFM27b/k4kHdCiVaj2J4x1dERKfq4MHkGA1UdIwRyMHCA
     FM27b/k4kHdCiVaj2J4x1dERKfq4oU2kSzBJMRkwFwYDVQQKExBORUNTVCBMYWJv
     cmF0b3J5MSwwKgYDVQQDEyNDZXJ0aWZpY2F0aW9uIEF1dGhvcml0eSBDZXJ0aWZp
     Y2F0ZYIJAOxEbwAjWP1CMAwGA1UdEwQFMAMBAf8wDQYJKoZIhvcNAQEFBQADgYEA
     rBSg7jZB8jg6cg1JDGnHBKNGrLS/ARgMFBTZfKIWI6Yp2gwYs856kdVKrlYSmU32
     lFMgHnQV6CbK9UKZtxhqmkfrwp70Frg5lSGmvvSBpuJOs2ZEUUHjJrEo3fHqDEvp
     v9q0dPcBNIX56v3XkqEnt8idicjjfLml3hBJQx0AKMs=
     -----END CERTIFICATE-----

How to Change your Account Password
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once you obtained access to the computing resources (as described in :ref:`access-facilities`), just connect to the lab wired network and point your browser to the user corner:

  https://home:8888

You can also use the wireless network, but this requires an extra step (described in :ref:`wifi`).

.. _extras:

Extras
~~~~~~

Need more resources or extra services?

Ask your tutor (see :ref:`tutors`) or the :ref:`radrl` and be ready to provide thorough motivation for your request. For instance, *"can I use machine X disk space for my project?"* is usually not enough. Explaining *why* you need *that* machine disk space and *which* is your project would be better in this case.

Computing Resources
-------------------

.. _lan:

Local Network
~~~~~~~~~~~~~

Each device connected to the wired network is assigned an IP address within the :kbd:`192.168.42.0/24` pool. Once connected, you can reach unauthenticated services and resources. However, most of the services and resources require authentication.

  .. note::

     Why we chose :kbd:`42` in :kbd:`192.168.42.0`?

     Because 42 is the `Answer to the Ultimate Question of Life, the Universe, and Everything <http://en.wikipedia.org/wiki/Answer_to_The_Ultimate_Question_of_Life,_the_Universe,_and_Everything#Answer_to_the_Ultimate_Question_of_Life.2C_the_Universe.2C_and_Everything_.2842.29>`_.

.. _IEEE 802.1X Standard: http://en.wikipedia.org/wiki/IEEE_802.1X

.. _wifi:

Wireless Access
~~~~~~~~~~~~~~~

We provide wireless access to the local network via WPA/WPA2 Enterprise (the ESSID is :kbd:`NECSTLab`). Access requires authentication, which is handled via `IEEE 802.1X Standard`_ and EAP-MSCHAPv2 protocols.

In short, you need an account (see :ref:`access-facilities`).

The setup instructions vary depending on the operating system:

* Windows XP (guide is forthcoming)

* Windows Vista/7

   * `Screencast (in Italian) <http://www.youtube.com/watch?v=pMDFYrHqozc>`_

* Windows 8 (guide is forthcoming)

* Debian/Ubuntu Linux (guide is forthcoming)

* Mac OS X (guide is forthcoming)

Once connected, your device is automatically granted :ref:`internet`.

.. _internet:

Internet Connectivity
~~~~~~~~~~~~~~~~~~~~~

We provide fast Internet connectivity from within the lab network. Wireless-connected devices are automatically granted connectivity: no extra steps are required.

Wire-connected devices must follow this procedure:

#. Follow this procedure: :ref:`access-facilities`.
#. Plug your laptop to any of the available cables.
#. Open your browser and connect to your favorite website via the HTTP scheme. This will pop up an authentication modal dialog: enter your credentials and your MAC address will be allowed. Sometimes, browsing a site through HTTPS does not correctly trigger the authentication dialog.

The network infrastructure of `Politecnico di Milano`_ is managed by `ASICT`_ and the bandwidth is provided the `GARR Consortium`_, the Italian Research & Education Network. Therefore, when using the Internet, in addition to the :ref:`rules`, every user should follow the `General Rules <http://www.wifi.polimi.it/en/regolamento/>`_.

The DHCP server automatically assigns to your device the default DNS server (see :ref:`dns`) and gateway, which is :kbd:`192.168.42.254`.

.. _dns:

DNS
~~~

We have an internal DNS server, :kbd:`192.168.42.254`, which provides two functions:

* internal queries for :kbd:`.necst.elet.polimi.it` domain names:

  #. :kbd:`192.168.42.254` is queried. In case of a cache hit, that is returned immediately, else

  #. :kbd:`192.168.42.1` is queried and the response is returned.

* caching of responses for queries to external domain names. A request to resolve follows this lifecycle:

  #. :kbd:`192.168.42.254` is queried. In case of a cache hit, that is returned immediately, else

  #. :kbd:`131.175.12.1` is queried and the response is returned.

  #. :kbd:`8.8.8.8` is queried and the response is returned.

Registring DNS Names
^^^^^^^^^^^^^^^^^^^^

Should you need to register your :kbd:`<myname>.necst.elet.polimi.it`, just send an email to `Federico Maggi`_ at `fede@maggi.cc <mailto:fede@maggi.cc?subject=[NECSTLab]%2-DNS%20name%20request>`_

Linux Shell
~~~~~~~~~~~

Your account includes a Linux shell, which is reachable via SSH at the following address:

  :kbd:`username@home.necst.elet.polimi.it`

or simply

  :kbd:`user@home`

Disk Quota
~~~~~~~~~~

Your account includes 5GB of storage space, which is reachable via SSH/SFTP as well as via CIFS/Samba share.

Remote Access via VPN
~~~~~~~~~~~~~~~~~~~~~

You can access the lab's internal resources remotely via our OpenVPN-based VPN. To obtain VPN access:

#. Obtain an account (see :ref:`access-facilities`)
#. Send an email to the :ref:`radrl`: `marco.santambrogio@polimi.it <mailto:marco.santambrogio@polimi.it?subject=[NECSTLab]%20VPN%20access%20request>`_

Printing
~~~~~~~~

There are two laser printers, one black-and-white printer and one color printer:

* Dell 2330dne (black and white): `drivers and instructions <http://www.dell.com/support/drivers/us/en/04/Product/dell-2330d>`_

* Samsung CLP-315 (color): `drivers and instructions <http://www.samsung.com/us/support/owners/product/CLP-315/XAA>`_

Access to the printers is granted via Samba within the :kbd:`micro` workgroup. You will need to authenticate first.

  .. note::

     Under Linux, you can configure the printer through CUPS. On most distributions, a simple way to install it is by using the web interface: point a browser to the URL http://localhost:631, and add a new printer under the tab Administration. Choose "Windows printer via SAMBA" as the type of network printer. You will then be asked for the connection URI, which contains your NECST username and password: 
     
          :kbd:`smb://username:password@home.necst.elet.polimi.it/printer`

     where :kbd:`printer` is either :kbd:`BlackAndWhite` or :kbd:`Color`. When asked to choose the model, provide the :kbd:`.ppd` file downloaded from the printer maker website.

  .. warning::
     In order not to waste paper and toner, prints are forced on both sides of each sheet. However, please limit the use of paper and toner (e.g., do not print your thesis).

Services
--------

.. _ml:

Mailing Lists and Communication
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There are several mailing lists. Depending on your work area, you should request access (or you already have access) to some of or all the following:

* `necst ml`_
* `necst-strut ml`_
* `necst-security-stud ml`_

In addition to these mailing lists, join our `NECSTLab Facebook Group`_.

.. _pm:

Project Management Platform
~~~~~~~~~~~~~~~~~~~~~~~~~~~

We rely on the `Redmine <http://www.redmine.org/>`_ to manage our projects. It provides:

* wikis
* source code repositories
* bug tracking
* gantt
* calendar
* news
* forums

If you are involved in a project and need to use any of the above tools, follow this procedure:

1. Obtain an account (see :ref:`access-facilities`)
2. Log in at

  https://redmine.necst.elet.polimi.it

3. Send an email to `Federico Maggi`_ with the :ref:`radrl` in Cc mentioning the name of the project you need access to: `fede@maggi.cc <mailto:fede@maggi.cc?subject=[NECSTLab]%20Redmine%20access%20request&amp;cc=marco.santambrogio@polimi.it>`_

Code Repositories: Git/SVN
~~~~~~~~~~~~~~~~~~~~~~~~~~

You can host your code in two places:

* our :ref:`pm` integrates a source code repository service:

  1. ask `Federico Maggi`_ for a new repository
  2. you will receive a path that looks like the following

    .. code-block:: none

       https://<username>@src.necst.elet.polimi.it/git/<project>/<repo-name>.git (Git)
       https://<username>@src.necst.elet.polimi.it/svn/<project>/<repo-name> (SVN)

  3. check out these guides if you are not sure how to use Git or SVN

    * `Git Immersion <http://gitimmersion.com/>`_
    * `Git Reference <http://gitref.org/>`_
    * `Version Control with Subversion <http://svnbook.red-bean.com/>`_ (long enough to discourage you from using SVN)
    * `Why Git is Better than X <http://thkoch2001.github.com/whygitisbetter/>`_

* the NECSTLab GitHub account, https://github.com/necst for which you need a personal GitHub account (free).

.. warning::
   Both the SVN and the internal Git repositories are accessed via HTTPS. Thus, bare in mind the :ref:`ssl`.

   The SVN client will show you the following warning

   .. code-block:: bash

      $ svn co https://user@src.necst.elet.polimi.it/svn/prj/repo
      Error validating server certificate for 'https://src.necst.elet.polimi.it:443':
       - The certificate is not issued by a trusted authority. Use the
         fingerprint to validate the certificate manually!
      Certificate information:
       - Hostname: src.necst.elet.polimi.it
       - Valid: from Mon, 23 Apr 2012 16:55:12 GMT
                until Sun, 06 Mar 2022 14:45:05 GMT
       - Issuer: NECST Laboratory
       - Fingerprint: dd:06:6f:a9:7b:bf:7e:6b:f0:85:f5:e1:ea:2c:e5:e5:85:da:58:14
      (R)eject, accept (t)emporarily or accept (p)ermanently?

   which you can safely accept (p) from within the lab local network.

   The Git client is particularly secure and prevents you from using a remote server at all if it has an non trusted certificate. It will show a message like the following:

   .. code-block:: bash

      $ git clone https://user@src.necst.elet.polimi.it/git/prj/repo.git
        Cloning into 'repo'...
        error: SSL certificate problem, verify that the CA cert is OK. Details:
        error:14090086:SSL routines:SSL3_GET_SERVER_CERTIFICATE:certificate
        verify failed while accessing https://user@src.necst.elet.polimi.it/git/
        prj/repo.git/info/refs?service=git-upload-pack
        fatal: HTTP request failed


   For Git, the best solution is to add the CA certificate to your computer's keychain (see :ref:`ssl`).

   There is also a workaround, which is although not secure:

   .. code-block:: bash

      $ GIT_SSL_NOVERIFY=true git clone \
          https://user@src.necst.elet.polimi.it/git/prj/repo.git

   or just export the :kbd:`GIT_SSL_NOVERIFY` variable to :kbd:`true` in your shell startup file (e.g., :kbd:`~/.bashrc`, :kbd:`~/.zshrc`).


Web Application Containers and HTTP Reverse Proxy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We can provide isolated containers to host your web applications written in Python, Ruby, PHP, Java, and so on. This is considered an non-ordinary service, although the lab is happy to provide it to you in case you need it for your thesis or your projects.

In addition, if you want your web application to be reachable from the outside network, we can provide port-forwarding and HTTP reverse proxy services.

Just follow this procedure if you want to know more: :ref:`extras`.

Centralized Logging and Exception Storage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Logging can be painful. It consumes space on your machine and, if not properly indexed, it takes ages to go through your logs to find the relevant details to debug your application. Also, logging is often not enough: what if an exception occurs? Do you have all the traceback information right in your logging messages? Unlikely.

Fortunately, we have set up two services:

* logstash, a tool for managing events and logs. You can use it to collect logs, parse them, and store them for later use (like, for searching).

  * How to reach it: http://logs.necst.elet.polimi.it
  * How to send logs to it: just configure your syslog to send logs to :kbd:`logs.necst.elet.polimi.it` via TCP port 55514

* Sentry, a tool for managing exceptions and storing the tracebacks for debugging

  * How to reach it: http://sentry.necst.elet.polimi.it
  * `How to send events to it <http://sentry.readthedocs.org/en/latest/client/index.html>`_

You need separate accounts for these tools. Ask `Federico Maggi`_ about this.

The NECSTCloud
--------------

We are thrilled to announce that we are currently working on building a powerful private cloud for the `NECSTLab`_, powered by `KVM <http://www.linux-kvm.org/>`_ and `OpenNebula <http://opennebula.org/>`_.
