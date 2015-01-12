.. -*- coding: utf-8 -*-

.. _facilities:

Facilities and Services: What's in the Lab
==========================================

The `NECSTLab`_ offers several facilities such as computing equipment, resources and services such as web hosting for small projects, code repositories.

Access to the facilities that require network connectivity is regulated by the :ref:`rules` and is granted once you obtain access to the lab (see :ref:`access`).

.. _access-facilities:

How to Obtain Access to the Computing Resources and Services
------------------------------------------------------------

Access to computing resources and services is regulated through individual accounts. To obtain an account, follow this procedure:

#. Obtain access to the lab (see :ref:`access`)
#. Send an email to `The System Administrator`_

Without an account, you are still allowed to connect to the local network via wired medium (see :ref:`lan`) and reach unauthenticated services and resources. However, most of the services and resources require authentication.

  .. warning::
     Please, do change your password!

.. _ssl:

Extras
~~~~~~

Need more resources or extra services?

Ask your tutor (see :ref:`tutors`) or the :ref:`radrl` and be ready to provide thorough motivation for your request. For instance, *"can I use machine X disk space for my project?"* is usually not enough. Explaining *why* you need *that* machine disk space and *which* is your project would be better in this case.

Computing Resources
-------------------

.. _lan:

Local Network
~~~~~~~~~~~~~

Just plug in your own computer to any available ethernet plug.

.. _wifi:

Wireless Access
~~~~~~~~~~~~~~~

Just connect to "polimi", "polimi-protected" (recommended) or "eduroam" following `these instruction`_.

Registring DNS Names
^^^^^^^^^^^^^^^^^^^^

Should you need to register your :kbd:`<myname>.necst.it`, just send an email to `Federico Maggi`_ at `sysadming@necst.it <mailto:sysadmin@necst.it?subject=[NECSTLab]%2-DNS%20name%20request>`_


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

* `NECSTLab Google Groups`_

In addition to these mailing lists, join our `NECSTLab Facebook Group`_.

.. _pm:

Code Repositories: Git
~~~~~~~~~~~~~~~~~~~~~~

You can host your code in two places:

* **private repos:** on https://bitbucket.org/necst - just create a Bitbucket account and as `The System Administrator`_ to be added to the team.

* **public repos:** we have a GitHub account, https://github.com/necst for which you need a personal GitHub account (free).


The NECSTCloud
--------------

We are running a beta version of a private cloud, to which you can request access by emailing `The System Administrator`_.
