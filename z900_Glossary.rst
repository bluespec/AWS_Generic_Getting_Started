.. include:: z00_Replacements.rsti

.. _Sec_Glossary:

========================================================================
Glossary
========================================================================

.. glossary::
   Access Key
    For ``ssh`` connections to AWS AMIs, and for any kind of
    programmatic interaction, utilities interaction, etc., AWS uses
    cryptographic access keys, not passwords. See :numref:`Sec_AMI`.

   AFI, AFI ID, AGFI ID
    AFI (Amazon FPGA Image) is Amazon's term for an FPGA bitfile (and
    its meta-data) that can be loaded into the FPGA of an F1 instance
    using AWS' command-line tools.

    AFIs are stored by Amazon somewhere in the AWS cloud; users
    typically do not directly see AFI files nor touch them.  Instead,
    we use the AWS CLI and AFI Management Tools to view an AFI,
    request Amazon to load it our FPGA, |ETC|, by providing a unique
    identifier.

    Amazon provides two identifiers for each AFI:

    * AFI ID: AFI Identifier. |EG| ``afi-0ef9bfe129ec102fd``
    * AGFI ID: Amazon Global FPGA Identifier. |EG| ``agfi-09cce6193e2a5ee67``

    Supposedly an AFI ID is "local" to an AWS geographic "region"
    whereas an AGFI ID is global across all regions.  It is not clear
    why AWS makes this distinction, instead of just using AGFI IDs
    everywhere.

   AFI Management Tools
    These are Amazon AWS tools for loading AFIs into the FPGA,
    examining its status, |ETC|

   AMI
    AMI (AWS Machine Instance) is a template of a virtual machine,
    from which you can create specific instances.  The template is
    typicallly pre-loaded with a standard operating system such as
    Ubuntu, Debian or CentOS Linux, and is often pre-loaded with other
    tools and utilities such as Vivado tools.  An AWS customer chooses
    an AMI from an AWS catalog of available AMIs, to create an
    instance.  See :numref:`Sec_AMI`.

   AWS
    Amazon Web Services.

   AWS CLI
    See "CLI" in this Glossary

   CLI
    AWS CLI is the Amazon Command-Line Interface for a wide variety of AWS services.
    These are Unix shell commands that begin with the word ``aws``.

   EC2
    EC2 (Elastic Computing) is Amazon's service for general purpose
    computation in the cloud. See :numref:`Sec_Setting_up_Instance`.

   F1 Instance
    See "Instance type" in this Glossary.

   FPGA
    Field Programmable Gate Array.

   Instance
    Synonym for "AMI", defined elsewhere in this glossary.

   Instance type
    The kind of physical machine on which your AMI runs (x86 vs. ARM,
    with specified amount of memory and disk space, and type of
    network connectivity).  See :numref:`Sec_AMI`.

    Instance types whose names begin with the letter "f" such as
    ``f1.2xlarge`` are called "F1 instances" and have an FPGA board
    attached to the server with a high-speed PCIe bus.

   Vivado
    Xilinx's tool for synthesizing RTL (Verilog, SystemVerilog) into a
    bitfile/AFI for the FPGA.
