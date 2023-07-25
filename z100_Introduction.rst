.. include:: z00_Replacements.rsti

.. _Sec_Intro:

================================================================
Introduction
================================================================

.. index:: ssh
.. index:: Ubuntu
.. index:: CentOS

.. _Sec_Overview_of_AWS_usage:

----------------------------------------------------------------
Overview of AWS usage
----------------------------------------------------------------

:numref:`Fig_AWS_Overview` shows an overview of how one uses AWS.

.. figure:: Figs/AWS_Overview.*
	    :width: 90%
	    :align: center
	    :name: Fig_AWS_Overview

	    Overview of AWS usage

From a local computer you use a web browser to visit the
aws.amazon.com web page, where you create accounts, see account
status, set up authentication credentials, |ETC| You also create one
or more "instances", which are virtual machines in the cloud.
Instances typically run standard, well-known operating systems.  In
this document we will only discuss the Ubuntu and CentOS operating
systems (both are variants of Linux).

Once your AWS account and instance are set up, you connect to the
instance in the usual way that you would connect to any remote
machine, |IE| using ``ssh`` from a terminal window, connecting you to
a ``bash`` shell in Linux on your instance (see
:numref:`Sec_connecting_to_an_instance`).

Connecting to an AWS instance requires cryptographic key-based
authentication (AWS does not support password-based authentication),
indicated by the `foo.pem` key file on your local machine in
:numref:`Fig_AWS_Overview`.

Once you have connected to your instance, you can use the operating
system in the usual way:

* Create and edit files
* Copy files to/from remote locations using ``scp``
* Clone remote git repositories
* |ETC|

You can also:

* Prepare a Verilog RTL design for the FPGA, and run it through the
  AWS synthesis flow (which uses Xilinx Vivado in batch mode, |IE| not
  the Vivado GUI).  The result is an AFI (AWS FPGA Image) representing
  the conventional FPGA bitfile.

* Load an AFI into the FPGA attached to your instance, at which point
  your design is "live" on the FPGA.

* Run software under Linux on your instance ("host-side") to interact
  with your design on the FPGA.
