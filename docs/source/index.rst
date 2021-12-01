`Computing Services <https://www.icds.psu.edu/computing-services/>`__

Roar Supercomputer Users’ Guide
===============================

0 We’re Redesigning the Roar User Guide!
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We’re currently working to revise the Roar User Guide with updated
content in an easier to use format, and we’d like your input!

All Roar users- students, faculty, and staff- are invited to take a
brief, five minute survey to help us

`Click here to take our Roar User Guide
survey. <https://pennstate.qualtrics.com/jfe/form/SV_7TBk5Pdt2rKiwTP>`__

1 Introduction
~~~~~~~~~~~~~~

Computational and data sciences are a fast growing mode of discovery, in
addition to traditional theory and experiment, because they provides a
unique virtual laboratory to investigate complex problems that are
otherwise impossible or impractical to address. Such problems can range
from understanding the physics of the origins of the universe, the
genomic/molecular basis of disease, or the socioeconomic impacts of a
digital society; to designing smart structures and nanoscale tailored
materials; or to developing systems for clean energy or realtime
responses to threats. The intellectual strength of computational science
lies with its universality – all research domains benefit from it. The
expectation is that The Institute for Computational and Data Sciences
will succeed both in facilitating research across a broad spectrum of
disciplines and in securing significant external resources for
cyberscience-related research for years to come.

1.1 What is Roar?
^^^^^^^^^^^^^^^^^

The Roar supercomputer (formerly known as the Institute for
Computational and Data Sciences Advanced CyberInfrastructure, or
ICDS-ACI) is our high-performance computing (HPC) infrastructure. The
name also refers to the services associated with this system. Roar
provides secure, high-quality advanced computing and storage resources
to the Penn State research community.

1.2 What does Roar do?
^^^^^^^^^^^^^^^^^^^^^^

Roar contributes to the ICDS mission by providing researchers with the
hardware, software, and technical expertise needed to solve problems of
scientific and societal importance. Roar provides a variety of services,
including operations, backup, technical consulting, and training. It
offers over 1000 servers with more than 23,000 processing cores, 6
Petabytes (PB) of disk parallel file storage, 12 PB of tape archive
storage, high-speed Ethernet and Infiniband interconnects, and a large
software stack. Roar is also compliant with specific NIH and NIST
security controls.

1.3 Our Mission
^^^^^^^^^^^^^^^

The mission of the Institute for Computational and Data Sciences is to
build capacity to solve problems of scientific and societal importance
through cyber-enabled research. As computation and data science become
increasingly vital modes of inquiry, we enable researchers to develop
innovative computational methods and to apply those methods to research
challenges. Specifically, we:

-  foster a collaborative, interdisciplinary scholarly community focused
   on the development and application of innovative computational
   methods;
-  expand participation in interdisciplinary research through strategic
   investments and effective outreach;
   and
-  provide a vibrant world-class cyberinfrastructure by maintaining and
   continually improving hardware and software solutions and technical
   expertise.

1.4 Our Vision
^^^^^^^^^^^^^^

ICDS will expand its role as an international leader in advancing
cyberinfrastructure along with computational and data-driven methods and
in driving their application to interdisciplinary research. We will use
our expertise coupled with our state-of-the-science research
infrastructure to support cyber-enabled interdisciplinary collaborations
and attract the worlds best researchers. These researchers will form a
vibrant intellectual community empowered to use the latest and most
effective computational methods to make transformative discoveries for
science and society.

2 Roar History
~~~~~~~~~~~~~~

In 2011 Penn State established an intra-university Cyberscience
Task-Force to develop a strategic and coherent vision for cyberscience
at the university. On the recommendations of this task-force, the
Institute for CyberScience was established in 2012. ICDS is one of seven
interdisciplinary research institutes under the Office of the Senior
Vice President for Research. Peer institutes include the Huck Institutes
of the Life Sciences, the Materials Research Institute, the Institutes
of Energy and the Environment, the Social Science Research Institute,
the Cancer Research Institute, and the Clinical and Translational
Science Institute.

Under its first director, Padma Raghavan, the institute began a cluster
hiring initiative in 2012-2013, in partnership with Penn State colleges
and institutes. This initiative, the `ICDS Co-hire
program <https://www.icds.psu.edu/about/icds-co-hires/>`__, brought in
promising computational experts from a range of fields.

In 2014 Executive Vice President and Provost Nick Jones and Vice
President for Research Neil Sharkey initiated a series of steps designed
to help Penn State deliver the broad spectrum of computing and data
services that are required to advance research. As part of this ongoing
process, ICDS continues to develop and sustain advanced
cyberinfrastructure, with the goal of accelerating research outcomes by
enhancing researcher productivity. In 2019, the institute was renamed to
be the Institute for Computational and Data Sciences. In 2020, the
supercomputer (formerly named the Institute for Computational and Data
Sciences Advanced Cyber Infrastructure, or ICDS-ACI) was renamed Roar.

3 System Overview
~~~~~~~~~~~~~~~~~

Roar is a heterogeneous cluster that consists of multiple node-types
connected to a common file system. The primary portions are ACI-b, the
batch portion of the cluster; ACI-i, the interactive portion; and the
data-manager nodes.

3.1 ACI-b
^^^^^^^^^

ACI-b, the batch portion of Roar, is used to submit jobs to dedicated
resources. ACI-b has the hostname

.. raw:: html

   <pre>submit.aci.ics.psu.edu</pre>

and can be logged into using ``ssh``. Users will be placed on a head
node, which is not intended for heavy processing. The head node should
only be used to submit jobs.

Typically, a job submission script including the resource requests and
the commands is submitted. A job scheduler will wait until dedicated
resources are available for this job. Jobs are submitted either to the
Open Queue allocation, which any Penn State student/faculty/staff are
able to use, or to a paid allocation. Jobs are typically submitted with
the qsub command:

.. raw:: html

   <pre>qsub subScript.pbs</pre>

3.1.1 Types of ACI-b Nodes
''''''''''''''''''''''''''

Compute resources are available in four configurations: Basic Memory,
Standard Memory, High Memory, and GPU.

.. raw:: html

   <table id="tablepress-4" class="tablepress tablepress-id-4">

.. raw:: html

   <thead>

.. raw:: html

   <tr class="row-1 odd">

.. raw:: html

   <th class="column-1">

Node Types

.. raw:: html

   </th>

.. raw:: html

   <th class="column-2">

Specifications

.. raw:: html

   </th>

.. raw:: html

   </tr>

.. raw:: html

   </thead>

.. raw:: html

   <tbody class="row-hover">

.. raw:: html

   <tr class="row-2 even">

.. raw:: html

   <td class="column-1">

Basic

.. raw:: html

   </td>

.. raw:: html

   <td class="column-2">

2.2 GHz Intel Xeon Processor, 24 CPU/server, 128 GB RAM, 40 Gbps
Ethernet

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr class="row-3 odd">

.. raw:: html

   <td class="column-1">

Standard

.. raw:: html

   </td>

.. raw:: html

   <td class="column-2">

2.8 GHz Intel Xeon Processor, 20 CPU/server, 256 GB RAM, FDR Infiniband,
40 Gbps Ethernet

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr class="row-4 even">

.. raw:: html

   <td class="column-1">

High

.. raw:: html

   </td>

.. raw:: html

   <td class="column-2">

2.2 GHz Intel Xeon Processor, 40 CPU/server, 1 TB RAM, FDR Infiniband,
10 Gbps Ethernet

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr class="row-5 odd">

.. raw:: html

   <td class="column-1">

GPU

.. raw:: html

   </td>

.. raw:: html

   <td class="column-2">

2.5 GHz Intel Xeon Processor, 2 Nvidia Tesla K80 computing
modules/server, 24 CPU/server, Double Precision, FDR Infiniband, 10 Gbps
Ethernet

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   </tbody>

.. raw:: html

   </table>

3.2 ACI-I
^^^^^^^^^

ACI-i provides a set of interactive cores that are configured as common
GUI interactive systems. ACI-i is a shared resource where users are
placed on an interactive node with other users.

ACI-i may only be `accessed via Open
OnDemand <https://www.icds.psu.edu/userguide/05-00-basics-aci-resources/05-04-connecting-aci/05-041-open-ondemand/>`__.

Often ACI-i is used to develop and test small scale test cases due to
the ability to use a graphical user interface. Once the model has been
developed, it can be submitted as a job to ACI-b to take advantage of
the greater computational resources available on ACI-b.

For example, a researcher might log in to ACI-i to develop a finite
element model using the graphical user interface for COMSOL. To test the
model, small simulations on a course mesh can be run on ACI-i. Then once
the model has been deemed satisfactory, the researcher can log in to
ACI-b to submit the COMSOL model using a much finer mesh.

Individual processes are limited to

-  4 processors
-  12 CPU hours per process
-  48 GB resident memory

on ACI-i. Note that the resident memory constraint still allows for
memory that can be sent to virtual memory during times of high usage.

3.3 Roar Open Queue
^^^^^^^^^^^^^^^^^^^

All Penn State students, faculty and staff are able to run on the Roar
“open queue” on ACI-b for no charge. The current limits per user on the
open queue are:

-  100 jobs pending
-  100 cores executing jobs at any given time
-  48-hour job wall-times
-  24-hour interactive session durations

Jobs requiring more time or processors than this are required to run on
an allocation.

Jobs running on the open allocation are placed on available compute
nodes. These are available as they are not being used by the group who
has an allocation reservation on that node. If that group does require
these resources, the running open queue jobs are pre-empted. Once the
allocation job has completed, your job will continue, if the code
running allows for this to occur.

ACI-i is open to any and all users, regardless of allocation.

3.4 HPRC
^^^^^^^^

HPRC is the hybrid-cloud portion of Roar, utilizing virtual cores at a
lower cost. HPRC jobs are submitted from ACI-b head nodes, with the host
name

.. raw:: html

   <pre>submit.aci.ics.psu.edu</pre>

…and can be logged into using ssh.

Users will be placed on a head node, which is not intended for heavy
processing. The head node should only be used to submit jobs.

Typically, a job submission script including the resource requests and
the commands is submitted. A job scheduler will wait until dedicated
resources are available for this job. Jobs are typically submitted with
the qsub command:

.. raw:: html

   <pre>qsub subScript.pbs</pre>

3.5 Filesystems
^^^^^^^^^^^^^^^

The Roar system has several filesystems available for users for active
and archival storage. Active storage can be utilized by running jobs and
archival storage is intended for long-term data storage.

| **Active Storage**
| All of the active storage is available from all of the Roar systems.
  Individual users have home, work and scratch directories that are
  created during account creation. The work and scratch directories
  should have links within the home directory, allowing for easy use. A
  user’s home directory is for personal files and cannot be shared. Work
  and scratch are able to be shared. Both home and work are backed up.
  Scratch is not backed up and files are subject to deletion 30 days
  after creation. *Do not keep important files on scratch.*

Group directories can be created to help facilitate research within a
group and can be purchased as an allocation. Note that individual
allocations will have separate locations within the group directory.

| **Archival storage**
| The archival storage is only available on the `Data
  Manager <#03-05-data-manager>`__ nodes. Archival storage can be
  purchased as an allocation.

By design, archival storage is best suited for storing relatively small
numbers of large files that will be accessed infrequently. Compared to
active storage, read and write performance in archive storage will be
very slow. Attempting to utilize archive storage when active storage
would be more appropriate can result in system degradations that
negatively impact all users of our shared system. Limiting files to a
minimum 1GB or 1000 per TB is a good rule of thumb.

+-----------+-----------+-----------+-----------+-----------+-----------+
| Space     | Location  | Quota     | File      | Backed-Up | File      |
|           |           |           | Limit     |           | Lifetime  |
|           |           |           |           |           | Limit     |
+===========+===========+===========+===========+===========+===========+
| Home      | /s        | 10 GB     | 500,000   | Yes       | None      |
|           | torage/ho |           |           |           |           |
|           | me/userID |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Work      | /s        | 128 GB    | 1,000,000 | Yes       | None      |
|           | torage/wo |           |           |           |           |
|           | rk/userID |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Scratch   | /g        | None      | 1,000,000 | No        | 30 Days   |
|           | pfs/scrat |           |           |           |           |
|           | ch/userID |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Group     | /         | 5 TB      | 1,000,000 | Yes       | None      |
|           | gpfs/grou | blocks    | per TB    |           |           |
|           | p/groupID |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Archive   | /archiv   | 5 TB      | Suggested | No        | None      |
|           | e/groupID | blocks    | lower     |           |           |
|           |           |           | limit of  |           |           |
|           |           |           | 1G/file   |           |           |
|           |           |           | or        |           |           |
|           |           |           | 1,000/TB  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+

3.6 Data Manager
^^^^^^^^^^^^^^^^

The data manager nodes are dedicated to file transfers, both within Roar
and between Roar and other systems. For active storage, it can be used
with command line file-transfer tools, such as ``rsync``, ``sftp`` or
``scp``, as well as with Globus, WinSCP, or FileZilla.

The data manager hostname is

.. raw:: html

   <pre>datamgr.aci.ics.psu.edu</pre>

For example, to connect to data manager, you can use the command

.. raw:: html

   <pre>ssh datamgr.aci.ics.psu.edu</pre>

to log in. After logging in, you can perform your file transfer.

**Important:** Do not use tools that attempt to mirror or replicate
directory and file trees (such as rsync) into archive storage. Using
such tools with archive storage can result in system degradations that
negatively impact all users of our shared system.

4 System Access
~~~~~~~~~~~~~~~

The Roar systems are available for all users with Penn State access.
Non-Penn State members who are collaborating with Penn State researchers
are able to get a Penn State SLIM access account and then sign up for a
Roar account.

4.1 Sponsorship
^^^^^^^^^^^^^^^

Each non-faculty member signing up for an account must have a sponsor.
This is typically the adviser or course instructor. The request requires
the Penn State username and not an alias. The `Penn State
directory <http://www.work.psu.edu/ldap/>`__ can be used to figure out
the username if only another email alias is known.

4.2 Permissions to use Resources
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The users who have access to an allocation are placed in an allocation
group. Users can see all of the groups they are in by using the ``id``
command.

To gain access to an allocation or a group storage, have the PI send an
email to the i-ASK Center (iask@ics.psu.edu) stating the user IDs (ex.
abc123) and the allocation(s) and group storage(s) you wish to add them
to. This explicit permission must be granted before users are allowed
access.

4.3 Getting an Account
^^^^^^^^^^^^^^^^^^^^^^

Users with a Penn State ID can sign up for an account using:
https://accounts.aci.ics.psu.edu

Faculty member accounts require no sponsorship. Students and staff
require a faculty sponsor, which must be listed by their original Penn
State ID, rather than by an alias. The sponsor will get an email stating
they were listed as a sponsor. The faculty member can respond to the
iAsk center (iAsk@ics.psu.edu) with either explicit approval or a
denial. If no denial is given, the student or staff member will be
granted implicit approval after two business days. Faculty members can
send an email with multiple users if they will be sponsoring multiple
accounts, such as for a class project. After an account has been
approved, it can take up to twenty-four hours before the system updates
and the user is able to login.

Users who do not have Penn State ID but are collaborators from other
institutions need to acquire a Penn State SLIM account before they sign
up for a Roar account and Duo. To request SLIM account, please follow
these
`instructions <https://www.icds.psu.edu/computing-services/account-setup/>`__.

You will need to wait for your SLIM access account to be created before
you can proceed to request your Roar account or sign up for two-factor
authentication.

5 Basics of the Roar Resources
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

5.1 System Usage
^^^^^^^^^^^^^^^^

The Roar system uses the Red Hat 7.9 Linux operating system with the
module system set up for software. All users will have to use the
terminal to access programs, including Open OnDemand users of ACI-i.

5.1.1 Shells
''''''''''''

Unix/Linux shells are command line interpreters that allow for a user to
interact with their operating system through utility commands and
programs. The Default Unix/Linux shell is BASH (the Bourne-Again SHell)
which has extensive online documentation, and common or necessary
commands are shown in the table below.

+-----------------------------------+-----------------------------------+
| Command                           | Description (For full             |
|                                   | documentation, use the command    |
|                                   | ‘man command’ to bring up the     |
|                                   | manual or find online             |
|                                   | documentation)                    |
+===================================+===================================+
| ls                                | The ‘list’ (ls) command is used   |
|                                   | to display all the files in your  |
|                                   | current directory. Using the ‘-a’ |
|                                   | flag will also show any hidden    |
|                                   | files (typically files beginning  |
|                                   | with a ‘.’ like .bashrc)          |
+-----------------------------------+-----------------------------------+
| cd                                | This is the ‘change directory’    |
|                                   | command. Use this to traverse     |
|                                   | directories (like ‘cd work’). To  |
|                                   | move back a directory level, use  |
|                                   | ‘cd..’.                           |
+-----------------------------------+-----------------------------------+
| mv                                | The ‘move’ command takes two      |
|                                   | arguments, the first being the    |
|                                   | file to move and the second being |
|                                   | the directory said file should be |
|                                   | moved to (‘mv file.txt            |
|                                   | /work/newdirectory/’). Note: ‘mv’ |
|                                   | can also be used to rename a file |
|                                   | if the second argument is simply  |
|                                   | a new file name instead of a      |
|                                   | directory.                        |
+-----------------------------------+-----------------------------------+
| mkdir                             | This command is used to make      |
|                                   | directories.                      |
+-----------------------------------+-----------------------------------+
| rmdir                             | This command is used to delete    |
|                                   | directories (‘rm -rf directory’   |
|                                   | would also work).                 |
+-----------------------------------+-----------------------------------+
| touch                             | This command is used to create    |
|                                   | files in a similar way to mkdir.  |
|                                   | (‘touch test.txt’ will create an  |
|                                   | empty text file named test).      |
+-----------------------------------+-----------------------------------+
| rm                                | This is the ‘remove’ command. As  |
|                                   | mentioned above, it can be used   |
|                                   | recursively to delete entire      |
|                                   | directory trees, or it can be     |
|                                   | used with no flags and a file as  |
|                                   | the argument to delete a single   |
|                                   | file.                             |
+-----------------------------------+-----------------------------------+
| locate                            | This command is used to locate    |
|                                   | files on a system. The flag ‘-i’  |
|                                   | will make the query case-         |
+-----------------------------------+-----------------------------------+
| insensitive, and asterisks (’*’)  |                                   |
| will indicate wildcard            |                                   |
| characters.                       |                                   |
+-----------------------------------+-----------------------------------+
| clear                             | Clears the terminal of all        |
|                                   | previous outputs leaving you with |
|                                   | a clean prompt.                   |
+-----------------------------------+-----------------------------------+
| history                           | Shows the previous commands       |
|                                   | entered.                          |
+-----------------------------------+-----------------------------------+
| find                              | Used for finding files, typically |
|                                   | with the -name flag and the name  |
|                                   | of the file.                      |
+-----------------------------------+-----------------------------------+
| grep                              | Used for searching within files.  |
+-----------------------------------+-----------------------------------+
| awk                               | A programming language typically  |
|                                   | used for data extraction.         |
+-----------------------------------+-----------------------------------+
| id                                | Show all of the groups a user is  |
|                                   | in.                               |
+-----------------------------------+-----------------------------------+
| du                                | Show the disk usage. Typically    |
|                                   | used with -h (for human readable) |
|                                   | and –max-depth=1 to limit to only |
|                                   | the directories in that level     |
|                                   | rather than all files.            |
+-----------------------------------+-----------------------------------+
| env                               | Print out all of the current      |
|                                   | environment variables.            |
+-----------------------------------+-----------------------------------+
| less                              | View a file.                      |
+-----------------------------------+-----------------------------------+
| cp                                | Copy a file. Note the -r          |
|                                   | (recursive) flag can be used to   |
|                                   | copy directories.                 |
+-----------------------------------+-----------------------------------+
| alias                             | Create an alias (something short) |
|                                   | that is interpreted as something  |
|                                   | else (a complicated command).     |
+-----------------------------------+-----------------------------------+
| pwd                               | Print the current working         |
|                                   | directory.                        |
+-----------------------------------+-----------------------------------+
| chmod                             | Change file permissions.          |
+-----------------------------------+-----------------------------------+
| chgrp                             | Change group for a file or        |
|                                   | directory.                        |
+-----------------------------------+-----------------------------------+
| ldd                               | Show the shared libraries         |
|                                   | required for an executable or     |
|                                   | library.                          |
+-----------------------------------+-----------------------------------+
| top                               | See the node usage. Often used    |
|                                   | with command U .                  |
+-----------------------------------+-----------------------------------+
| /usr/bin/time                     | Show time and memory statistics   |
|                                   | for a command being run. Often    |
|                                   | used with the -v (verbose) flag.  |
+-----------------------------------+-----------------------------------+
| bg                                | Continue running a paused task in |
|                                   | the background                    |
+-----------------------------------+-----------------------------------+
| fg                                | Bring a background task into the  |
|                                   | foreground                        |
+-----------------------------------+-----------------------------------+
| Ctrl + c                          | Kill a process.                   |
+-----------------------------------+-----------------------------------+
| Ctrl + z                          | Suspend a process                 |
+-----------------------------------+-----------------------------------+
| Ctrl + r                          | Search through your history for a |
|                                   | command that includes the text    |
|                                   | typed next.                       |
+-----------------------------------+-----------------------------------+
| \* \* \*                          | \* \* \*                          |
+-----------------------------------+-----------------------------------+

There are also some special characters to be aware of that will be
helpful.

-  ``~`` is your home directory
-  ``.`` means here
-  ``..`` means up one directory
-  ``*`` is the wildcard: ``*`` for all files or ``*.png`` for all png
   files
-  ``|``\ is pipe (send the output to another command)
-  ``>`` means write command output to a file (Example: ``ls > log.ls``)

Most commands have a manual that show all of the different ways the
command can be used. For example,

.. raw:: html

   <pre>man ls</pre>

shows all of the info for the ``ls`` command. You can use the arrows to
scroll through the manual and the letter ``q`` for quit. Some commands
will also provide a shortened version of the manual showing the
available flags if an incorrect flag is used. For example,

.. raw:: html

   <pre>mam-list-funds -banana</pre>

brings up a list of all of the flags available for ``mam-list-funds``.
Any non-working flag will allow for this. Note that this doesn’t give
information about what the flags do, just what the flags are. This may
be enough to remind you of something you had done previously.

| All shells utilize configuration files. For BASH, this is split
  between 2 files: ``~/.bash_profile`` and ``~/.bashrc``.
| (NOTE: ``~/`` in Linux is a way to specify your own home directory!).
  The ``.bash_profile`` file is always parsed when a terminal is open,
  including with an SSH session. To connect the two in such a way that
  ``.bashrc`` will always be sourced for a session, make sure this code
  is included in your ``~/.bash_profile``:

.. raw:: html

   <pre>if [ -f ~/.bashrc ]; then . ~/.bashrc fi</pre>

5.1.2 Alternative Shells
''''''''''''''''''''''''

BASH is only the default shell, and it doesn’t come with quite a few
features that many Linux power-users would like to have on the
command-line. Other common shells include KSH (KornSHell), ZSH (Z
SHell), and FISH (Friendly-Interface SHell). These shells all have
documentation available online regarding their installation and
customization.

5.1.3 Environmental Variables
'''''''''''''''''''''''''''''

Environment variables are values that pertain to certain aspects of an
operating system’s configurations. These variables are typically used by
utilities and programs for things like finding out where the user’s home
directory is (``$HOME``) or where to look for executable files
(``$PATH``). The prompt for BASH is held as the variable ``PS1``.

You can print the environment variable to the screen using the ``echo``
command:

.. raw:: html

   <pre>echo $HOME</pre>

A good way to view environment variables that are set is by using the
``env`` command

.. raw:: html

   <pre>env</pre>

which outputs all of the variables currently in use.

To change the value of an existing variable or to create and set a new
variable, we use ``export``. For example, to set a variable called
``workDir`` to a directory called here within your home directory, the
command would be:

.. raw:: html

   <pre>export workDir=$HOME/here</pre>

Once this environment variable is set, you are able to use this. For
example, to change to this directory, the command would be:

.. raw:: html

   <pre>cd $workDir</pre>

For something like PATH where you really do not want to overwrite what
values are already stored, you can append values with

.. raw:: html

   <pre>export PATH=$PATH:/new/dir/path/</pre>

In lists of values, the colon (``:``) is used as the delimiter. The
dollar sign (``$``) is used to reference variables, so that export
command essentially appends the new directory to the list of existing
directories searched for executables. It is possible to prepend as well,
which may come in handy if you compile a different version of an
existing command.

For more general reading on environment variables in Linux, see these
pages on
`variables <http://tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_02.html>`__
and `environmental
variables <https://en.wikipedia.org/wiki/Environment_variable>`__.

The environment variables allow for script portability between different
systems. By referencing variables like the home directory ($HOME) you
can generalize a script’s functionality to work across systems and
accounts.

+-----------------------------------+-----------------------------------+
| Variable Name                     | Description                       |
+===================================+===================================+
| USER                              | Your user ID                      |
+-----------------------------------+-----------------------------------+
| HOSTNAME                          | The name of the server that the   |
|                                   | script is being run on            |
+-----------------------------------+-----------------------------------+
| HOME                              | Your home directory               |
+-----------------------------------+-----------------------------------+
| WORK                              | Your work directory               |
+-----------------------------------+-----------------------------------+
| SCRATCH                           | Your scratch directory            |
+-----------------------------------+-----------------------------------+
| TMPDIR                            | The directory in which a job’s    |
|                                   | temporary files are placed        |
|                                   | (created and deleted              |
|                                   | automatically)                    |
+-----------------------------------+-----------------------------------+

5.1.4 References
''''''''''''''''

The Linux terminal and submitting jobs are not unique to Roar. You can
find many different training resources online for these. The Linux
foundation offers `free
training <https://training.linuxfoundation.org/free-linux-training>`__.
Lots of great information and tutorials for everyone from beginner Linux
user to advanced users can be found
`here <https://www.linux.org/pages/download/>`__. Linux has been around
for a long time. Therefore, any problem you might be having, someone has
probably already had. It is always worthwhile to look around `stack
exchange <https://unix.stackexchange.com/>`__ to see if your question
has already been answered.

5.2 Module System
^^^^^^^^^^^^^^^^^

Roar now uses the Lmod environment modules system. Environment Modules
provide a convenient way to dynamically change the users environment
through modulefiles. This includes easily adding or removing directories
to the ``PATH``, ``LD_LIBRARY_PATH``, ``MANPATH``, and ``INFOPATH``
environment variables. A modulefile contains the necessary information
to allow a user to run a particular application or provide access to a
particular library. All of this can be done dynamically without logging
out and back in. Modulefiles for applications modify the users path to
make access easy. Modulefiles for library packages provide environment
variables that specify where the library and header files can be found.
Learn more about modules on `TACC’s
website <https://www.tacc.utexas.edu/research-development/tacc-projects/lmod>`__.

5.2.1 Module Families
'''''''''''''''''''''

Roar uses module families for compilers and parallelization libraries.
Modules that are built with a parent module, such as a compiler, are
only available when the parent module is loaded. For example, the
version of LAPACK built with the gcc module is only available when the
gcc module is located.

A good way to illustrate how the module families work is to view the
available modules before a family is loaded as well as after. You can do
this with the gcc family by inspecting the output of

.. raw:: html

   <pre class="script">module purge

   module avail

   module load gcc/8.3.1

   module avail

   </pre>

5.2.2 Using Modules
'''''''''''''''''''

You can load modules into your environment with the command with the
module load command. For example, to load the gcc module, you can use
the command:

.. raw:: html

   <pre>module load gcc/8.3.1</pre>

Note that the version number is not required. Each software will have a
default module that will be loaded if no version number is provided.
However, it is recommended that you put the version number so that you
know and have a record of what version is being used.

You can view the modules that you currently have open using the module
list command:

.. raw:: html

   <pre>module list</pre>

You can also unload modules that you do not need in the same way:

.. raw:: html

   <pre>module unload gcc/8.3.1</pre>

It is also possible to remove all of your loaded modules at once using
purge:

.. raw:: html

   <pre>module purge</pre>

5.2.3 Querying Modules
''''''''''''''''''''''

You can view the available modules using the command:

.. raw:: html

   <pre>module avail</pre>

Note that this only looks at the available modules, which may be limited
by module family based on modules are currently loaded. You can search
all of the modules using ``module spider``. For example, to search for
VASP, you can use the command

.. raw:: html

   <pre>module spider vasp</pre>

which will search through all module names and module files to return
anything related to vasp.

| The module can be used to give you information about the software
  using the module show command. For
| example, the information about the hdf5 module, which was built using
  the gcc module, can be seen using the commands:

.. raw:: html

   <pre class="script">module load gcc/8.3.1

   module show hdf5/1.10.7

   </pre>

The output of this is shown:

.. raw:: html

   <pre class="script">---------------------------------------------------------------------

   /opt/aci/modulefiles/Compiler/gcc/8.3.1/hdf5/1.10.7.lua:

   ---------------------------------------------------------------------

   help([[HDF5 is a unique technology suite that makes possible the management of extremely large and complex data collections. The HDF5 technology suite includes: A versatile data model that can represent very complex objects and a variety of metadata. A completely portable file format with no limit on the number or size of data objects in the collection. A software library that runs on a range of computational platforms, from laptops to massively parallel systems, and implements a high-level API with C, C++, Fortran 90, and Java interfaces. A rich set of integrated performance features that allow for access time and storage space optimizations. Tools and applications for managing, manipulating, viewing, and analyzing the data in the collection.
   ]])

   whatis("Description: HDF5 is a unique technology suite that makes possible the management of extremely large and complex data collections.")

   whatis("URL: https://support.hdfgroup.org/HDF5/")

   prepend_path("PATH","/opt/aci/sw/hdf5/1.8.18_gcc-8.3.1/bin")

   prepend_path("LD_LIBRARY_PATH","/opt/aci/sw/hdf5/1.8.18_gcc-8.3.1/lib64")

   prepend_path("C_INCLUDE_PATH","/opt/aci/sw/hdf5/1.8.18_gcc-8.3.1/include")

   prepend_path("CPLUS_INCLUDE_PATH","/opt/aci/sw/hdf5/1.8.18_gcc-8.3.1/include")

   prepend_path("LIBRARY_PATH","/opt/aci/sw/hdf5/1.8.18_gcc-8.3.1/lib64")

   pushenv("HDF5","/opt/aci/sw/hdf5/1.8.18_gcc-8.3.1")

   pushenv("HDF","/opt/aci/sw/hdf5/1.8.18_gcc-8.3.1")

   </pre>

Note that this tells you some information about the software, gives a
website for more help and shows the environment variables that are
modified. The environment manipulation section can be very helpful for
users who are compiling codes and linking to libraries as these paths
indicate where the relevant objects may be found.

5.2.4 Controlling Modules Loaded at Login
'''''''''''''''''''''''''''''''''''''''''

Most shells have a configuration file that allows you to set aliases
(nicknames for commands both simple or complex), set environment
variables, and automatically execute programs and commands. In this case
we are interested in the last mentioned feature: automating commands at
login. For BASH there are two files at play: ``~/.bash_profile`` and
``~/.bashrc.`` To force your bashrc to be sourced in every opened
terminal and SSH session, include this code in your bash_profile:

.. raw:: html

   <pre>if [ -f ~/.bashrc ]; then

   . ~/.bashrc

   fi
   </pre>

Once that has been done, you can add whatever automated module loads you
want in the .bashrc file by including:

.. raw:: html

   <pre>module load <module name>/<version></pre>

The version specification is optional, excluding it will cause whatever
the default version is to be loaded. Other shells have similar
configuration methods that are detailed in online documentation.

5.3 Connecting to ACI-b
^^^^^^^^^^^^^^^^^^^^^^^

Users can connect to ACI-b with the hostname

.. raw:: html

   <pre>submit.aci.ics.psu.edu</pre>

using ``ssh``. Users connecting with ssh are encouraged to use the
secure x-window forwarding flag (``-Y``) if x-windows will be used
during the session. Note that the screen may not show \* symbols for
each keystroke when your password is being entered. (In this example,
the username is “abc123”.)

.. raw:: html

   <pre>ssh -Y abc123@submit.aci.ics.psu.edu</pre>

5.4 Connecting to ACI-i
^^^^^^^^^^^^^^^^^^^^^^^

Users connect to ACI-i with Open OnDemand.

5.4.1 Open OnDemand
^^^^^^^^^^^^^^^^^^^

Open OnDemand lets you utilize Penn State’s high performance computing
resources in a graphical, menu-based environment that doesn’t require
using an ssh client. Interacting with Roar with Open OnDemand looks and
feels like the desktop or web-based applications you’re used to.

| Open OnDemand is accessed through your web browser, so there’s nothing
  to download or install.
| Simply go to this web address:

PORTAL.ACI.ICS.PSU.EDU

**Note:** When accessing Roar on Open OnDemand, you’ll see a CILogon
screen before you can enter your Penn State ID and password. Simply
click the **Log On** button to proceed.

Introduction to Using Open OnDemand on Roar (formerly known as ICDS-ACI)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. raw:: html

   <iframe loading="lazy" src="https://www.youtube.com/embed/ekiz0o94pwQ" allowfullscreen="allowfullscreen" width="560" height="315" frameborder="0">

﻿

.. raw:: html

   </iframe>

5.5 Connecting to HPRC
^^^^^^^^^^^^^^^^^^^^^^

Users can connect to HPRC from ACI-b head nodes, with the host name

.. raw:: html

   <pre>submit.aci.ics.psu.edu</pre>

…using ssh. Users connecting with ssh are encouraged to use the secure
x-window forwarding flag (-Y) if x-windows will be used during the
session. Note that the screen may not show \* symbols for each keystroke
when your password is being entered. (In this example, the username is
“abc123”.)

.. raw:: html

   <pre>ssh -Y abc123@submit.aci.ics.psu.edu</pre>

5.6 Transferring Data to and from Roar
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

There are many different ways to transfer data to and from Roar.

5.6.1 Command line File Transfer
''''''''''''''''''''''''''''''''

There are two main command-line SSH commands to transfer files: ``scp``
and ``sftp``. ``scp`` is a non-interactive command that takes a set of
files to copy on the command line, copies them, and exits. ``sftp`` is
an interactive command that opens a persistent connection through which
multiple copying commands can be performed.

| **scp**
| To copy one or more local files up to the Roar server, the ``scp``
  syntax would be:

.. raw:: html

   <pre>scp local_file <username>@datamgr.aci.ics.psu.edu:<target_directory></pre>

The default port for scp is set to 22. If you use this port you will be
automatically directed to Duo Push authentication during 2FA.

For user abc123 to copy the local files foo.c and foo.h into their home
directory on the host aci-b.aci.ics.psu.edu, the following command would
be used:

.. raw:: html

   <pre>[abc123@local ~]$ scp foo.c foo.h abc123@datamgr.aci.ics.psu.edu:~/.</pre>

The -r (recursive) flag can be used to transfer directories.

.. raw:: html

   <pre>[abc123@local ~]$ scp -r dirA abc123@datamgr.aci.ics.psu.edu:~/.</pre>

Users can also copy files from Roar onto their own computer using

.. raw:: html

   <pre>[abc123@local ~]$ scp abc123@datamgr.aci.ics.psu.edu:~/fileA .</pre>

| **sftp**
| ``sftp`` is an interactive command that uses the same syntax as a
  standard command-line ftp client. It differs from a standard ftp
  client in that the authentication and the data transfer happen through
  the SSH protocol rather than the FTP protocol. The SSH protocol is
  encrypted whereas the FTP protocol is not.

There are a number of basic commands that are used inside of ``stfp``:

-  ``put filename``: uploads the file filename
-  ``get filename``: downloads the file filename
-  ``ls``: lists the contents of the current remote directory
-  ``lls``: lists the contents of the current local directory
-  ``pwd``: returns the current remote directory
-  ``lpwd``: returns the current local directory
-  ``cd directory``: changes the current remote directory to directory
-  ``lcd directory``: changes the current local directory to directory

The syntax for calling ``sftp`` is:

.. raw:: html

   <pre>sftp username@hostname</pre>

To choose between different options for 2FA you have to set the port to
1022 using P flag similar to ``ssh``.

An example ``sftp`` session, with both the inputs and outputs, would be:

.. raw:: html

   <pre class="script">[abc123@local ~]$ sftp abc123@submit.aci.ics.psu.edu

   Connecting to submit.aci.ics.psu.edu...

   Password: <user abc123 password>

   # Duo Push authentication

   Connected to aci-b.aci.ics.psu.edu.

   sftp> pwd

   Remote working directory: /storage/home/abc123

   sftp> lpwd

   Local working directory: /home/abc123

   sftp> cd work/depot

   sftp> pwd

   Remote working directory: /storage/work/abc123/depot

   sftp> lcd results

   sftp> lpwd

   Local working directory: /home/abc123/results

   sftp> ls -l

   -rw-r--r--

   1 root

   root

   5 Mar

   3 12:08 dump

   sftp> lls -l

   total 0

   sftp> get dump

   Fetching /storage/work/abc123/depot/dump to dump

   /storage/work/abc123/depot/dump

   100%

   5

   0.0KB/s

   0.0KB/s

   00:00

   sftp> lls -l

   total 4

   -rw-r--r-- 1 abc123 abc123 5 Mar

   3 12:09 dump

   sftp> put data.txt

   Uploading data.txt to /storage/work/abc123/depot/data.txt

   data.txt

   100%

   15

   0.0KB/s

   sftp>

   </pre>

| **rsync**
| ``rsync`` is a utility that can be used to copy files and for keeping
  files the same on different systems as a rudimentary version control
  system. The benefit to using ``rsync`` over ``scp`` is that if an
  ``scp`` is stopped for any reason (poor wireless connection, large
  files, etc) the restart will begin as if no files were copied over.
  The ``rsync`` utility will only copy the files that were not
  successfully moved over in the previous command. Once you have SSH
  access between two machines, you can synchronize dir1 folder ( home
  directory in this example) from local to a remote computer by using
  syntax:

.. raw:: html

   <pre>rsync -a ~/dir1 username@remote_host:destination_directory</pre>

where remote host is the Roar host name as in scp command. If dir1 were
on the remote system instead of the local system, the syntax would be:

.. raw:: html

   <pre>rsync -a username@remote_host:/home/username/dir1 place_on_local_machine</pre>

If you are transferring files that have not been compressed yet, like
text files, you can reduce the network transfer by adding compression
with the ``-z`` option:

.. raw:: html

   <pre>rsync -az source_dir username@remote_host:target_dir</pre>

The -P flag is very helpful. It combines the flags –progress and
–partial. The former gives you a progress bar for the transfers and the
latter allows you to resume interrupted transfers:

.. raw:: html

   <pre>rsync -azP source_dir username@remote_host:target_dir</pre>

In order to keep two directories synchronized it is necessary to delete
files from the destination directory if they are removed from the
source. rsync does not delete anything from the destination directory by
default. To change this behavior use the ``–delete`` option:

.. raw:: html

   <pre>rsync -a --delete source_dir username@remote_host:taget_dir</pre>

If you wish to exclude certain files or directories located inside a
directory you are syncing, you can do so by specifying them in a
comma-separated list following ``–exclude=`` option:

.. raw:: html

   <pre>rsync -a --exclude=pattern_to_exclude source_dir username@remote_host:target_dir

   </pre>

One common pitfall that can affect users transferring files between
systems with different usernames and groups can be the permissions
assigned to the files being ``rsync``-ed. The ``--chmod`` option can be
used both to set the permissions for the user, group and other
independently, as well as to set any directory permissions for
inheritance of files created within the directory after the transfer is
complete. Multiple commands can be strung together using commas. For
example, the following will provide full permissions for the user, read
and execute permissions for others in the group and will cause all of
the future files created within any directories being transferred to
inherit the group that the directory has.

.. raw:: html

   <pre>rsync -a--chmod u=rwx,g=rx,Dg+s source_dir username@remote_host:target_dir</pre>

5.6.2 Graphical File Transfer
'''''''''''''''''''''''''''''

WinSCP and FileZilla provide a free secure FTP (SFTP) and secure copy
(SCP) client with graphical interface for Windows, Linux and Mac using
SSH, allowing users to transfer files to and from our cluster file
system using a drag-and-drop interface. Please use either the SCP or
SFTP protocol with port 22 with the data manager nodes

.. raw:: html

   <pre>datamgr.aci.ics.psu.edu</pre>

to transfer files. Please note that your two factor authentication is
required.

For more information, please visit the `WinSCP
homepage <http://winscp.net/eng/index.php>`__ or the `FileZilla
homepage <https://filezilla-project.org/>`__.

You can see the connection process in this `ICDS tutorial
video <https://www.youtube.com/watch?v=pOJaKeA89lI&t=2s>`__.

It is also possible to use the online interface for either Box or
DropBox within Firefox on ACI-i for users who logged on with Open
OnDemand. It is not currently possible to sync to your storage space on
Roar at this time.

5.6.3 Web-based Services
''''''''''''''''''''''''

Globus is one of the recommended methods of transferring very large
data. Most HPC centers have endpoints set up allowing for optimized
transfer between large centers. Users can also install personal
endpoints on their own machines using Globus Connect. Its web interface
allows users to transfer files from a desktop or mobile device.

Users must sign up for a `globus <http://globus.org>`__
`account <http://globus.org>`__ as this is a separate service from Roar.
An endpoint is a location to/from which the files are to be transferred.
There are 2 types of endpoints: server endpoints (like Roar) and
personal endpoints (user’s laptop). To save or bookmark endpoints go to
Manage Endpoints section on the globus webpage (you have to be logged
in). Then click add Globus Connect Personal In Step 1 you have to define
the name for your personal endpoint and click on Generate Setup Key.
Copy the key to the clipboard. In Step 2 you have to download and
install Globus Connect Personal app appropriate for your OS. To finish
the installation you will be asked to paste the generated key which you
copied to the clipboard. Each time you want to transfer file you will
have to have the Globus Connect Personal running on your local computer.
If you do not have a Globus account, create one
`here <https://www.globus.org.>`__. Set up a free Globus Online account
using your PSU ID. If you wish to use Globus to transfer data to/from
your local computer, install the Globus Connect Personal tool on your
computer. More information on the Instructions for Installing Globus
Connect Personal tool for linux can be found
`here. <https://docs.globus.org/how-to/globus-connect-personal-linux/>`__
Instructions for
`mac <https://docs.globus.org/how-to/globus-connect-personal-mac/>`__
and
`windows <https://docs.globus.org/how-to/globus-connect-personal-windows/>`__
are also available.

On the Globus Start Transfer page, choose one of three Roar end points
(for example ``PennState_ICS-ACI_DTN_EndPnt_01``) as the end point on
one side. This will pull up an authentication window. Use your Penn
State ID for the user name, and your Penn State ID password for the pass
phrase. This will set up an authenticated session.

Select and authenticate with the other endpoint for your transfer, and
initiate your transfer. You may need to click on refresh list if you
can’t see the transferred files despite the transfer has completed.

There are other specialized data-transfer software available for
specific needs, such as Aspera. Contact the iAsk center if you have any
questions regarding using one of these specialized tools on ACI.

5.6.4 File Permissions
''''''''''''''''''''''

File permissions can be seen using the ``-l`` flag for ls:

.. raw:: html

   <pre>ls -l</pre>

The letters at the beginning indicate the file or folder permissions
while the third and fourth columns show the owner and group associated
with the file. The letters used are typically rwx, for read, write and
execute. These are grouped in sets of three, the first set for the
owner, the second for the group and the third for the entire world.
Users may change permissions using the chmod command. An excellent
overview of how to change permissions using chmod can be found
`here. <http://catcode.com/teachmod/>`__

Users may also want to change the group of their files using the
``chgrp`` command.

6 Application Development
~~~~~~~~~~~~~~~~~~~~~~~~~

6.1 Version Control
^^^^^^^^^^^^^^^^^^^

Version control is a way to track multiple versions of a code. This has
a place in development, primarily with adding new features while still
using the original code or with multiple developers, and if the code has
minor variants for reasons such as slightly different input/output data
types or for use on different compute resources. One popular version
control tool is ``git``, which uses a distributed approach which allows
for many development points. The basic ``git`` workflow is to

-  Modify files – create new code, fix bugs, etc.
-  Stage the files – explicitly state what will be deposited
-  Commit your files – store a snapshot

Your repository will have a master branch, where the current production
code usually exists, and other branches that may be for any other
purpose, such as development or variations. Branches can either be
merged back to the master branch as features are added and execution is
validated, or kept separate if the usage requires multiple working
versions of the code. It is up to the user to define how their
repository is set-up as well as to keep non-local versions of the
repository as up-to-date as desired. There are great online resources
for ``git`` including `excellent
documentation <http://git-scm.com/doc>`__ and
`tutorials <http://try.github.io>`__.

6.2 Basic Compilation
^^^^^^^^^^^^^^^^^^^^^

You can your own compile code for running on Roar. A basic compilation
might look like

.. raw:: html

   <pre>gcc -O2 -lm -o hello.out hello.c <\pre></pre>

where the gnu compiler is used to compile a C code in the file hello.c.

-  ``gcc`` Compiler being used
-  ``-O2`` Optimization Flag
-  ``-lm`` Link to the math library
-  ``-o hello.out`` Output file
-  ``hello.c`` Input file

It’s possible to link to pre-compiled libraries that are created by you
or that already exist on the system. The ``module show`` command can be
very useful in determining the locations of the libraries and header
files required to compile codes. You can link in a variety of ways.

-  ``-L`` (as in Love) Path to a directory containing a library
-  ``-l`` (as in love) Library name
-  ``-I`` (as in Iowa) Path to header files

Complicated compilations can also be done using a build automation
software package such as ``make``, which is available without a module,
or ``cmake``, which is available as a module. The general build
automation process involves using a Makefile that has:

-  Outputs – the executable/library being created
-  Dependencies – what each output relies on
-  Instructions – how to make/find each dependency

and can set environment variables. The nomenclature for repeated
sections can use regex and so can be very complicated. Information about
these tools can be found in online references, such as the
`make <http://gnu.org/software/make/manual/make.html>`__ and
`cmake <https://cmake.org/documentation/>`__ manuals. Some common
pitfalls that the iAsk center sees for using make are:

-  Makefiles require tabs and not spaces at the beginning of indented
   lines
-  The ``-j`` flag and an integer can be used to compile on multiple
   processors
-  The ``-f`` flag can be used to specify the name of the makefile if
   not Makefile
-  Some makefiles are configured for the compute environment. You may
   need to use the command ``./configure`` if there isn’t a make file
   and configure scripts exist./li>

It is possible to either make the output file directly executable and
add the location to your path to call this from anywhere, or to execute
the output from the location of the file directly. For our hello example
from before, this can be done using the command ``./hello.out`` from the
directory in which the executable exists.

6.3 Libraries
^^^^^^^^^^^^^

Roar offers many optimized libraries for users to link to. Please see
the most common libraries listed below.

6.3.1 MKL
'''''''''

Intel Math Kernel Library (MKL) consists of commonly used mathematical
operations in computational science. The functions in MKL are optimized
for use on Intel processors. More information can be found
`here. <https://software.intel.com/en-us/mkl>`__

The MKL module can be loaded using the command

.. raw:: html

   <pre>module load mkl</pre>

6.3.2 LAPACK
''''''''''''

LAPACK (Linear Algebra Package) is a software library used for numerical
linear algebra. It can handle many common numerical algebra computations
such as solving linear systems, eigenvalue problems, and matrix
factorization. It depends on BLAS. More information can be found on the
`website. <http://www.netlib.org/lapack/>`__

You can load the LAPACK module using the commands:

.. raw:: html

   <pre>module load gcc/5.3.1
   module load lapack/3.6.0
   </pre>

6.3.3 BLAS
''''''''''

BLAS (Basic Linear Algebra Subprograms) is a collection of low level
matrix and vector operations such as vector addition, scalar
multiplication, matrix multiplication, etc. For more information, refer
to this `link. <http://www.netlib.org/blas/>`__

The BLAS module can be loaded with the command

.. raw:: html

   <pre>module load blas</pre>

6.3.5 Boost
'''''''''''

Boost is a C++ library that contains many useful functions covering a
wide range of applications such as linear algebra and multithreading.
More information can be found `here. <http://www.boost.org/>`__

You can load Boost with the command

.. raw:: html

   <pre>module load boost</pre>

6.3.6 PETsc
'''''''''''

The Portable, Extensible Toolkit for Scientific Computation (PETsc,
pronounced PET-see) is a suite of data structures and routines for
solving partial differential equations and sparse matrices in a parallel
fashion that is scalable. It was developed by Argonne National
Laboratory.

You can load the PETsc module using the command

.. raw:: html

   <pre>module load petsc/3.8.3</pre>

More information on features, tutorials, manuals, etc can be found on
the `website. <http://www.mcs.anl.gov/petsc/>`__

7 Running Jobs on ACI-b
~~~~~~~~~~~~~~~~~~~~~~~

Jobs are submitted from the head nodes of ACI-b and will run when
dedicated resources are available on the compute nodes. Roar uses Moab
and Torque for the scheduler and resource manager. Jobs can be either
run in batch or interactive modes. Both are submitted using the qsub
command.

7.1 Requesting Resources
^^^^^^^^^^^^^^^^^^^^^^^^

Both batch and interactive jobs are required to provide a list of
requested resources to the scheduler in order to be placed on a compute
node with the correct resources available. These are given either in the
submission script or on the command line. If these are given in a
submission script, they must come before any non-PBS command.

Typical PBS directives are:

+-----------------------------------+-----------------------------------+
| PBS Directive                     | Description                       |
+===================================+===================================+
| #PBS -l walltime=HH:MM:SS         | This specifies the maximum wall   |
|                                   | time (real time, not CPU time)    |
|                                   | that a job should take. If this   |
|                                   | limit is exceeded, PBS will stop  |
|                                   | the job. Keeping this limit close |
|                                   | to the actual expected time of a  |
|                                   | job can allow a job to start more |
|                                   | quickly than if the maximum wall  |
|                                   | time is always requested.         |
+-----------------------------------+-----------------------------------+
| #PBS -l pmem=SIZEgb               | This specifies the maximum amount |
|                                   | of physical memory used by any    |
|                                   | processor ascribed to the job.    |
|                                   | For example, if the job would run |
|                                   | on four processors and each would |
|                                   | use up to 2 GB (gigabytes) of     |
|                                   | memory, then the directive would  |
|                                   | read #PBS -l pmem=2gb. The        |
|                                   | default for this directive is 1   |
|                                   | GB of memory.                     |
+-----------------------------------+-----------------------------------+
| #PBS -l mem=SIZEgb                | This specifies the maximum amount |
|                                   | of physical memory used in total  |
|                                   | for the job. This should be used  |
|                                   | for single node jobs only.        |
+-----------------------------------+-----------------------------------+
| #PBS -l nodes=N:ppn=M             | This specifies the number of      |
|                                   | nodes (nodes=N) and the number of |
|                                   | processors per node (ppn=M) that  |
|                                   | the job should use. PBS treats a  |
|                                   | processor core as a processor, so |
|                                   | a system with eight cores per     |
|                                   | compute node can have ppn=8 as    |
|                                   | its maximum ppn request. Note     |
|                                   | that unless a job has some        |
|                                   | inherent parallelism of its own   |
|                                   | through something like MPI or     |
|                                   | OpenMP, requesting more than a    |
|                                   | single processor on a single node |
|                                   | is usually wasteful and can       |
|                                   | impact the job start time.        |
+-----------------------------------+-----------------------------------+
| #PBS -l nodes=N:ppn=M:O           |                                   |
+-----------------------------------+-----------------------------------+

Node types available on Roar:

============= =========================== =============
Node Type = O CPU                         RAM
============= =========================== =============
basic         Intel Xeon E5-2650v4 2.2GHz 128 GB Total
lcivybridge                               
scivybridge   Intel Xeon E5-2680v2 2.8GHz 256 GB Total
schaswell     Intel Xeon E5-2680v3 2.5GHz 256 GB Total
himem         Intel Xeon E7-4830v2 2.2GHz 1024 GB Total
============= =========================== =============

7.1.1 Sample Batch Submission Script
''''''''''''''''''''''''''''''''''''

The following is a submission script for a Matlab job that will run for
5 minutes on one processor using the open queue.

.. raw:: html

   <pre class="script">#!/bin/bash

   #PBS -l nodes=1:ppn=1

   #PBS -l walltime=5:00

   #PBS -A open

   # Get started

   echo "Job started on $(hostname) at $(date)"

   # Load in matlab

   module purge

   module load matlab

   # Go to the correct place

   cd $PBS_O_WORKDIR

   # Run the job itself - a matlab script called runThis.m

   matlab-bin -nodisplay -nosplash < runThis.m > log.matlabRun

   # Finish up

   echo "Job Ended at $(date)"

   </pre>

This script would be submitted using the command

.. raw:: html

   <pre>qsub subScript.pbs</pre>

from the directory containing the submission and matlab scripts.

7.2 Interactive Compute Sessions on ACI-b
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Interactive jobs may be submitted to ACI-b using the -I (for
interactive) flag. Interactive jobs require resource requests and an
allocation. An interactive job can be submitted using a command similar
to:

.. raw:: html

   <pre>qsub -A open -l walltime=1:00:00 -l nodes=1:ppn=2 -I</pre>

The job will be given a job ID and your session will wait until this job
has the resources to start. You will then be placed on the compute node
and given a usable terminal session within your current session. For
example a user submitting an interactive job may see

.. raw:: html

   <pre class="script">[abc123@aci-lgn-001 ~]$ qsub I l nodes=1:ppn=1 l walltime=4:00:00 -A open

   qsub: waiting for job <span style="word-wrap: break-word;">2449840.torque01.util.production.int.aci.ics.psu.edu</span> u to start

   qsub: job <span style="word-wrap: break-word;">2449840.torque01.util.production.int.aci.ics.psu.edu</span> ready

   [abc123@comp-bc-0267 ~]$

   </pre>

Note that the node the user is on changes from log-in node (aci-lgn-001)
to a basic core compute node (comp-bc-0267) when the job starts. You can
ask for x-windows to be displayed using the ``-X`` flag with the
``qsub`` command, as long as you have logged into ACI-b using the ``-Y``
flag with ``ssh``. Note that some users experiencing difficulty with
interactive x-windows on ACI-b jobs will often use an Open OnDemand
interactive session to connect to ACI-i, and then ``ssh`` with the
``-Y`` flag to ACI-b from ACI-i.

It is recommended that you compile your code using an interactive job on
the nodes that your job will run.

7.3 PBS Environmental Variables
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Jobs submitted will automatically have several PBS environment variables
created that can be used within the job submission script and scripts
within the job. A full list of PBS environment variables can be used by
viewing the output of

.. raw:: html

   <pre>env | grep PBS > log.pbsEnvVars</pre>

run within a submitted job.

+-----------------------------------+-----------------------------------+
| Variable Name                     | Description                       |
+===================================+===================================+
| PBS_O_WORKDIR                     | The directory in which the qsub   |
|                                   | command was issued.               |
+-----------------------------------+-----------------------------------+
| PBS_JOBID                         | The job’s id.                     |
+-----------------------------------+-----------------------------------+
| PBS_JOBNAME                       | The job’s name.                   |
+-----------------------------------+-----------------------------------+
| PBS_NODEFILE                      | A file in which all relevant node |
|                                   | hostnames are stored for a job.   |
+-----------------------------------+-----------------------------------+

7.3.1 Viewing and Deleting Jobs
'''''''''''''''''''''''''''''''

There are several ways to view existing jobs. The ``qstat`` command can
give some basic information about your own queued and running jobs.

.. raw:: html

   <pre>qstat</pre>

Some helpful flags are ``-u`` (user), ``-s`` (status), ``-n`` (to show
the nodes running jobs are placed on) and -f to show more information
for a specified job. For example, to view more information about job
536, you can use the command

.. raw:: html

   <pre>qstat -f 536</pre>

Common status for jobs are Q for queued, R for running, E for ending, H
for being held and C for complete.

You can also view all of the jobs running, waiting and being held using
the showq command:

.. raw:: html

   <pre>showq</pre>

It may be helpful for you to view all of the jobs running on an
allocation. For example, if you are a member of the
abc123_a_g_sc_default allocation, you can view the running and queued
jobs using the command:

.. raw:: html

   <pre>showq -w acct=abc123_a_g_sc_default</pre>

You may delete your jobs using the qdel command. For example, the job
546 may be deleted using the command:

.. raw:: html

   <pre>qdel 546</pre>

Jobs that are not responding may require being purged from the nodes.
You can do this with the ``-p`` flag:

.. raw:: html

   <pre>qdel -p 546</pre>

Note that you are only able to delete your own jobs, not other users.

7.3.2 Additional Job Information
''''''''''''''''''''''''''''''''

You can use the checkjob command to view some additional information
about queued and running jobs. For example, to give very verbose
information about job 548, you can use the command:

.. raw:: html

   <pre>checkjob 548 -v -v</pre>

7.4 GReaT Allocations
^^^^^^^^^^^^^^^^^^^^^

All jobs submitted to an allocation that have available resources are
guaranteed to start within 1 hour. Note that the resources include both
available hours as well as the requested resources. For example, a group
that has a 40 core allocations on two standard memory nodes is limited
to the RAM and CPUs on both nodes. Single processor jobs that request
most of the memory on the nodes may block other jobs from running, even
if CPUs are idle.

Users submitting to an allocation can run in ‘burst’ mode. Your group
may use a number of cores up to four times your Core Limit (referred to
as your 4x Core Limit). When your group submits jobs that exceed your
Core Limit, you are considered to be ‘bursting,’ and your jobs will run
on our Burst Queue. Bursting consumes your allocation faster than
normal. How much you can burst is determined by your 90-day sliding
window.

How much you can use Roar is governed by the size of your allocation and
how much you have used the system in the past 90 days. In any given
90-day period, you may use up to your Core Limit times the number of
hours in 90 days (2160). The amount of core-hours you have available is
governed by a 90-day sliding window, such that the core-hours you use in
any given day become available again after 90 days.

**How is My Allocation “Charged” for a Batch Job?**

The charge associated with a job is dependent on the total number of
requested cores and the actual runtime of the job (in seconds):

NumberOfCores*Runtime.

For example, if a 20 core job has a total runtime of 1 hour the charge
to the GReaT allocation is 20*3600=7200 core seconds. Please note that
the charge includes the number of requested cores, not the number of
utilized cores. Additionally, the requested walltime and actual runtime
of the job may differ.

**Note:** In the tables below, run times are noted in hours to simplify
the examples. In practice, allocations are charged for usage by the
second.

Example: If you have a 20-core allocation, you can consume 43,200 (20 \*
2160) core-hours within any given 90-day period. Your average rate of
usage in any 90-day period cannot exceed 20 cores per hour. Core-hours
you use on the first day of your allocation will become available again
on the 91st day; core-hours you use on the second day become available
again on the 92nd day; and so on. If you never burst, you can use all
your cores continuously.

Example: With your 20-core allocation, you run jobs requiring 20 cores
continuously. In any given 90-day period, you will use 43,200
core-hours, and your average rate of usage is 20 cores per hour.

=== ==================== =================== ========================
Day Core-Hours Available Usage on this Day   Core-Hours Used This Day
=== ==================== =================== ========================
1   43,200               20 cores x 24 hours 480
2   42,720               20 cores x 24 hours 480
3   42,240               20 cores x 24 hours 480
4   41,760               20 cores x 24 hours 480
=== ==================== =================== ========================

Usage continues at the same rate of 20 cores, 24 hours per day.

=== ==================== =================== ========================
Day Core-Hours Available Usage on this Day   Core-Hours Used This Day
=== ==================== =================== ========================
90  480                  20 cores x 24 hours 480
91  480                  20 cores x 24 hours 480
92  480                  20 cores x 24 hours 480
=== ==================== =================== ========================

Note that on Day 91, the core-hours used on Day 1 become available
again; on Day 92, the core-hours used on Day 2 become available again;
and so on.

Example: Bursting above your allocation may lead to days with 0 hours
available.

=== ==================== =================== ========================
Day Core-Hours Available Usage on this Day   Core-Hours Used This Day
=== ==================== =================== ========================
1   43,200               20 cores x 24 hours 480
2   42,720               80 cores x 24 hours 1920
3   40,800               80 cores x 24 hours 1920
4   38,8801,760          80 cores x 24 hours 1920
=== ==================== =================== ========================

Usage continues at the same rate of 80 cores, 24 hours per day.

=== ==================== ================== ========================
Day Core-Hours Available Usage on this Day  Core-Hours Used This Day
=== ==================== ================== ========================
24  480                  60 cores x 8 hours 480
25  0                    0                  0
26  0                    0                  0
=== ==================== ================== ========================

At this point, no core-hours are available, and no jobs can be run
against the allocation until Day 91, when the core-hours used on Day 1
become available again.

=== ==================== =================== ========================
Day Core-Hours Available Usage on this Day   Core-Hours Used This Day
=== ==================== =================== ========================
91  480                  20 cores x 24 hours 480
92  1920                 0                   0
93  3840                 20 cores x 24 hours 480
=== ==================== =================== ========================

Identifying Allocation Usage:

Users are able to see their allocations with the balance using the
command mam-list-funds. This is typically used with the -h flag to show
the allocation and balance in hours.

.. raw:: html

   <pre>mam-list-funds -h</pre>

The allocation topology, end date and node-type can be shown using the
mam-list-accounts command.

.. raw:: html

   <pre>mam-list-accounts</pre>

Note that this shows you expired allocations as well. The second column
(Active) will show True for active allocations and False for expired
allocations.

Users interested in their own usage may want to investigate several of
the other mam commands:

.. raw:: html

   <pre>mam-list-usagerecords
   mam-list-transactions
   </pre>

7.5 ACI-b GPU nodes
^^^^^^^^^^^^^^^^^^^

The ACI-b GPU nodes are comprised of dual NVIDIA Tesla K80 GPU cards.
Each card contains two GPUs that are individually schedulable. These
nodes contain dual E5-2680 processors (24 total cores), and 256GB of
RAM. For more information on this hardware, refer to `NVIDIA’s K80
specification
document <https://www.nvidia.com/content/dam/en-zz/Solutions/Data-Center/tesla-product-literature/Tesla-K80-BoardSpec-07317-001-v05.pdf>`__.

7.5.1 Accessing GPU Resources
'''''''''''''''''''''''''''''

| To access a GPU on ACI-b, you must be a member of a GReAT GPU
  allocation. To request a node with a GPU, add *“gpus=N”* to your
  resource list in either your job script or a submission argument. For
  example, ``#PBS -l nodes=1:ppn=1:gpus=1`` or
  ``qsub -l nodes=1:ppn=1:gpus=1 ...``
| The requested GPU is placed in exclusive process mode by default. This
  means that only a single process can access the GPU, but it can spawn
  multiple different threads. To allow multiple processes on a single
  GPU, the “shared” feature can be appended to the resource list. A
  general GPU request then takes the form of:
| ``#PBS -l nodes=NN:ppn=NC:gpus=NG:feature``
| or
| ``qsub -l nodes=NN:ppn=NC:gpus=NG:feature``
| Where:

-  NN = the number of nodes
-  NC = the number of cores per node
-  NG = the number of GPUS per node
-  feature = shared or is not included

| **GPU job script example**
| Here is an example GPU job script that requests a single GPU and
  simply calls nvidia-smi:

.. raw:: html

   <pre class="script">#!/bin/bash
   #PBS -l nodes=1:ppn=1:gpus=1
   #PBS -l walltime=2:00
   #PBS -l pmem=1gb
   #PBS -A gpu_allocation_name

   # Get started
   echo " "
   echo "Job started on `hostname` at `date`"
   echo " "

   # Go to the submission directory
   cd $PBS_O_WORKDIR

   # Run the main job commands
   nvidia-smi

   # Finish up
   echo " "
   echo "Job Ended at `date`"
   </pre>

7.5.2 GPU Monitoring
''''''''''''''''''''

You may want to monitor the status of a node’s GPU. The nvidia-smi
command provides basic monitoring capabilities and will provide
information such as GPU and memory utilization, power consumption,
running processes, etc. Example output for this command:

.. raw:: html

   <pre class="script">$ nvidia-smi
   Mon Oct  8 15:03:53 2018
   +-----------------------------------------------------------------------------+
   | NVIDIA-SMI 390.30                 Driver Version: 390.30                    |
   |-------------------------------+----------------------+----------------------+
   | GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
   | Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
   |===============================+======================+======================|
   |   0  Tesla K80           Off  | 00000000:05:00.0 Off |                    0 |
   | N/A   41C    P0    63W / 149W |      0MiB / 11441MiB |      0%   E. Process |
   +-------------------------------+----------------------+----------------------+
   |   1  Tesla K80           Off  | 00000000:06:00.0 Off |                    0 |
   | N/A   36C    P0    71W / 149W |      0MiB / 11441MiB |      0%   E. Process |
   +-------------------------------+----------------------+----------------------+
   |   2  Tesla K80           Off  | 00000000:84:00.0 Off |                    0 |
   | N/A   40C    P0    59W / 149W |      0MiB / 11441MiB |      0%   E. Process |
   +-------------------------------+----------------------+----------------------+
   |   3  Tesla K80           Off  | 00000000:85:00.0 Off |                    0 |
   | N/A   32C    P0    75W / 149W |      0MiB / 11441MiB |     81%   E. Process |
   +-------------------------------+----------------------+----------------------+

   +-----------------------------------------------------------------------------+
   | Processes:                                                       GPU Memory |
   |  GPU       PID   Type   Process name                             Usage      |
   |=============================================================================|
   |  No running processes found                                                 |
   +-----------------------------------------------------------------------------+
   </pre>

7.5.3 CUDA
''''''''''

| NVIDIA has developed a parallel computing platform and programming
  model to facilitate the use of GPUs in general computing. This comes
  in the form of both GPU-accelerated libraries as well as programming
  extensions for C, C++, and Fortran (PGI compilers). CUDA 8.0, 9.0, and
  9.1 are installed on the gpu nodes at /usr/local. To set up your shell
  environment, the CUDA bin and lib64 directories need to be added to
  PATH and LD_LIBRARY_PATH.
| ``$ export PATH=/usr/local/cuda-9.1/bin:$PATH   $ export LD_LIBRARY_PATH=/usr/local/cuda-9.1/lib64:$LD_LIBRARY_PATH``
| **CUDA example**
| The CUDA Toolkit includes many CUDA code examples that can help get
  you started with writing your own CUDA-enabled software. These
  examples can be found at /usr/local/cuda/samples/ for the latest
  available version of CUDA. You may also find `additional CUDA code
  samples <https://developer.nvidia.com/cuda-code-samples>`__ on the
  NVIDIA website.
| Here, we will compare the performance of the CPU and GPU for the
  “nbody” example.

1. Start an interactive session on a GPU node
   ``$ qsub -I -A gpu_allocation_name -l nodes=1:ppn=1:gpus=1 -l pmem=10gb -l walltime=1:00:00``
2. Set up the environment
   ``$ export PATH=/usr/local/cuda-9.1/bin:$PATH       $ export LD_LIBRARY_PATH=/usr/local/cuda-9.1/lib64:$LD_LIBRARY_PATH       $ export CPATH=/usr/local/cuda-9.1/samples/common/inc:$CPATH``
3. Copy the nbody source code to your ACI work directory
   ``$ mkdir ~/work/cuda_example && cd ~/work/cuda_example       $ cp /usr/local/cuda-9.1/samples/5_Simulations/nbody/ .``
4. Compile the nbody example
   ``$ cd nbody       $ make``
5. Compare GPU vs CPU timing
   ``CPU:       $ ./nbody -benchmark -numbodies=1024 -cpu``\ GPU:
   $ ./nbody -benchmark -numbodies=1024 -numdevices=1

**CUDA resources**

-  XSEDE course:
   `slides <https://drive.google.com/file/d/12TwgVcVqoW8T9eyz7RuYQ9yw_si8kbA4/view>`__
   and
   `video <https://www.youtube.com/watch?v=2R5R0nXm3xc&feature=youtu.be>`__
-  `NVIDIA Education &
   Training <https://developer.nvidia.com/cuda-education-training>`__
-  `Virtual Workshop <https://cvw.cac.cornell.edu/GPU/default>`__

7.5.4 OpenACC
'''''''''''''

OpenACC is an API comprised of compiler directives (similar to OpenMP)
that enable programmers to specify portions of code (C, C++, and
Fortran) to be executed on a GPU (or other accelerators). OpenACC
compiler support will be available on the Roar systems with the release
v18.5 of the PGI compilers. This section will be expanded once the PGI
compilers are released.

7.5.5 GPU Enabled Applications
''''''''''''''''''''''''''''''

Some software packages available on the Roar software stack have native
GPU support, as indicated in the table below. For a full description of
available functionality, please consult each package’s software
documentation.

+-----------------------------------+-----------------------------------+
| Software                          | Information                       |
+===================================+===================================+
| Matlab                            | `MathWorks: Getting started with  |
|                                   | GPUs <https://mathworks.          |
|                                   | com/discovery/matlab-gpu.html>`__ |
+-----------------------------------+-----------------------------------+
| Mathematica                       | `Wolfram: GPU                     |
|                                   | computing <                       |
|                                   | https://reference.wolfram.com/lan |
|                                   | guage/guide/GPUComputing.html>`__ |
+-----------------------------------+-----------------------------------+
| Ansys: APDL                       | ansys192 -acc nvidia -na N …      |
+-----------------------------------+-----------------------------------+
| Ansys: Fluent                     | fluent -gpgpu=N …                 |
+-----------------------------------+-----------------------------------+
| Ansys: polyflow                   | polyflow -acc nvidia -na N …      |
+-----------------------------------+-----------------------------------+
| Ansys: other                      | The -batchoptions command flag    |
|                                   | can be used to enable GPU         |
|                                   | support. See the software         |
|                                   | specific manual available through |
|                                   | the GUI for the options available |
|                                   | for each Ansys product.           |
+-----------------------------------+-----------------------------------+

ex. ansysedt -batchoptions “HFSS/EnableGPU=1” …\| \|Abaqus|abaqus gpus=N
… OR abaqus -gpus N …\|

where N = the number of GPU devices

| **Python TensorFlow example**
| TensorFlow is a popular open-source machine learning and deep learning
  library originally developed by Google. The API is typically used with
  Python, for which there is GPU support. The following example will
  walk through the local installation and testing of the GPU-enabled
  version of TensorFlow.

1. Start an interactive session on a GPU node
   ``$ qsub -I -A gpu_allocation_name -l nodes=1:ppn=1:gpus=1 -l pmem=10gb -l walltime=1:00:00``
2. Create a conda environment for tensorflow-gpu
   ``$ cd ~/work       $ mkdir conda_gpu_tensorflow && cd conda_gpu_tensorflow       $ mkdir $PWD/conda_pkgs       $ export CONDA_PKGS_DIRS=$PWD/conda_pkgs       $ module load python/3.6.3-anaconda3       $ conda create -y --prefix $PWD       $ source activate $PWD``
   (Use ``source deactivate`` to exit the conda environment.)
3. Install the cudatoolkit for python. The version of cudatoolkit must
   be compatible with the GPU driver version. The current driver
   (390.30) supports up to CUDA 9.1.
   ``$ conda install -y cudatoolkit=9.0``
4. Install tensorflow-gpu. Note that the packaged binaries were not
   compiled with optimized instruction sets such as AVX, AVX2, etc. To
   compile your own version of tensorflow from source, see the official
   `TensorFlow
   documentation <https://www.tensorflow.org/install/source>`__.
   ``$ conda install --no-update-dependencies -y tensorflow-gpu``
5. Run the GPU test model. The average performance should be ~5,300
   examples/sec for a single GPU.
   ``$ git clone https://github.com/tensorflow/models.git``
   ``$ python models/tutorials/image/cifar10/cifar10_train.py``

8 Running Jobs on HPRC
~~~~~~~~~~~~~~~~~~~~~~

HPRC jobs are submitted from the head nodes of ACI-b and will run when
available resources are available on the compute nodes. Roar uses Moab
and Torque for the scheduler and resource manager. Jobs can be either
run in batch or interactive modes. Both are submitted using the qsub
command.

.. _requesting-resources-1:

8.1 Requesting Resources
^^^^^^^^^^^^^^^^^^^^^^^^

| Whether you are submitting batch or interactive jobs, you are required
  to provide a list of requested resources to the scheduler. These are
  given either in the submission script or on the command line. If these
  are given in a submission script, they must come before any non-PBS
  command. Current limits on HPRC resource requests:
| • Pmem < 8GB
| • Mem < 160GB
| • Core/node <= 20
| • Node = 1

8.1.1 Sample HPRC Batch Submission Script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

| The following is a submission script for a Matlab job that will run
  for 5 minutes on one processor. Note that an allocation is required to
  submit jobs to HPRC. Users familiar with submitting jobs to ACI-b will
  note only minor differences in this script.
| ``#!/bin/bash   #PBS -l nodes=1:ppn=1   #PBS -l walltime=5:00   #PBS -q hprc``

``#PBS -A ics-hprc   # Get started   echo "Job started on ‘hostname‘ at ‘date‘"   # Load in matlab   module purge   module load matlab   # Go to the correct place   cd $PBS_O_WORKDIR   # Run the job itself - a matlab script called runThis.m   matlab-bin -nodisplay -nosplash < runThis.m > log.matlabRun   # Finish up   echo "Job Ended at ‘date‘"``

8.2 Interactive Compute Sessions on HPRC
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Interactive jobs may be submitted to HPRC using the -I (for interactive)
flag. Interactive jobs require resource requests and an allocation. An
interactive job can be submitted using a command similar to:

``qsub -I -A ics-hprc -q hprc -l nodes=1:ppn=20 -l mem=32gb -l walltime=1:23:30:00``

The job will be given a job ID, and your session will wait until this
job has the resources to start. You will then be placed on the compute
node and given a usable terminal session within your current session.
For example, a user submitting an interactive job may see:

| \`[abc123@aci-lgn-008 abc123]$ qsub -I -A ics-hprc -q hprc -l
  nodes=1:ppn=20 -l mem=32gb -l walltime=1:23:30:00
| qsub: waiting for job
  12907285.torque01.util.production.int.aci.ics.psu.edu to start
| qsub: job 12907285.torque01.util.production.int.aci.ics.psu.edu ready
| [abc123@comp-vc-1645 abc123]

To enable X11 forwarding to the interactive job, include the -x flag
(output will be identical to above):

``qsub -I -x -A ics-hprc -q hprc -l nodes=1:ppn=20 -l mem=32gb -l walltime=1:23:30:00``

8.3 Requesting a Custom Singularity Container on HPRC
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Jobs on HPRC are run in an enterprise Linux 6 container. If you want
your job to run in a custom Singularity container, you can specify that
container either on the qsub command line or within your script.

Here is an example on the qsub command line:

``qsub -I -v SINGULARITY_CONTAINER="/storage/work/abc123/singularity/bionic-base.simg"``

For example, the above interactive job would provide:

``[abc123@aci-lgn-008 abc123]$ qsub -I -A ics-hprc -q hprc -l nodes=1:ppn=20 -l mem=32gb -l walltime=1:23:30:00   qsub: waiting for job 12907285.torque01.util.production.int.aci.ics.psu.edu to start   qsub: job 12907285.torque01.util.production.int.aci.ics.psu.edu ready   [abc123@comp-vc-1645 abc123]$ cat /etc/os-release   NAME="Ubuntu"   VERSION="18.04.1 LTS (Bionic Beaver)"   ID=ubuntu   ID_LIKE=debian   PRETTY_NAME="Ubuntu 18.04.1 LTS"   VERSION_ID="18.04"   HOME_URL="https://www.ubuntu.com/"   SUPPORT_URL="https://help.ubuntu.com/"   BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"   PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"   VERSION_CODENAME=bionic   UBUNTU_CODENAME=bionic``

Here is an example where the container is specified within your
submission script:

``#PBS -l walltime=1:30:00   #PBS -l nodes=1:ppn=8   #PBS -l mem=8gb   #PBS -j oe   #PBS -r n   #PBS -m bae   #PBS -M abf123@psu.edu   #PBS -q hprc   #PBS -A ics-hprc   #PBS -v SINGULARITY_CONTAINER="/storage/work/abc123/singularity/bionic-base.simg"``

8.4 Specifying a Custom Bash Environment on HPRC
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Some jobs may be best served by custom bash environments, especially
those run within containers that do not support modules or other
environment variables supported on ACI-b directly. A custom bash
environment can be specified with a qsub variable on the command line or
within your submission script.

Here’s an example on the command line:

``qsub -I -v SINGULARITY_CONTAINER="/storage/work/abc123/singularity/bionic-base.simg" -v BASH_ENV=”/storage/abc123/.bashrc_ubuntu” -q hprc -A epo2-hprc -l nodes=1:ppn=20 -l pmem=5gb -l walltime=16:30:00``

Here’s an example within the submission script:

``#PBS -l walltime=1:30:00   #PBS -l nodes=1:ppn=8   #PBS -l mem=8gb   #PBS -j oe   #PBS -r n   #PBS -m bae   #PBS -M abf123@psu.edu   #PBS -q hprc   #PBS -A ics-hprc   #PBS -v SINGULARITY_CONTAINER="/storage/work/abc123/singularity/bionic-base.simg"   #PBS -v BASH_ENV=”/storage/abc123/.bashrc_ubuntu”``

9 Software Stack
~~~~~~~~~~~~~~~~

ICDS has a software policy that explains the details of how software can
be used. The policy can be read on `our policy
page <https://www.icds.psu.edu/computing-services/ics-aci-policies/>`__.

9.1 User Stack
^^^^^^^^^^^^^^

Users are able to install software into their own home and work
directories as well as in group spaces. ICDS strongly recommends that
research groups who compute in multiple locations do this for all of
their software so that the version can be consistent across platforms.

The i-ASK Center can provide guidance for the installation of many
software packages.

9.2 System Stack
^^^^^^^^^^^^^^^^

Many commonly used applications are built and maintained by the system.

9.2.1 System Stack Requests
'''''''''''''''''''''''''''

Requests for software to be placed on the system stack can be made to
the i-ASK Center. Users requesting software should show the reason for
the request, typically due to licensing issues or because of the broad
user base across campus.

9.3 System Stack Applications
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Because of the module families, it is hard to view all of the available
software on the system. The software list can be found on the `software
stack webpage <https://www.icds.psu.edu/computing-services/software/>`__
or by looking in the directory where the software modules are:

.. raw:: html

   <pre>ls /opt/aci/sw/</pre>

9.3.1 COMSOL
''''''''''''

To open COMSOL, first log into ACI-i using Open OnDemand. More
information regarding how to do this can be found in `section
5.4.1 <https://www.icds.psu.edu/computing-services/ics-aci-user-guide/#05-04-connecting-aci>`__.
Next open a terminal by going to the top left corner and clicking on

.. raw:: html

   <pre>Applications -> System Tools -> Terminal</pre>

In the terminal window type the following commands:

.. raw:: html

   <pre>module load comsol
   comsol
   </pre>

The graphical user interface for COMSOL should now be opened and COMSOL
can be used as usual. However, it is worth mentioning that ACI-i is only
intended to run short jobs. Often researchers will use ACI-i to develop
and test their COMSOL models before submitting them as jobs on the more
computational powerful ACI-b cluster. Running a COMSOL model on the
ACI-b system is a relatively straightforward process. To do so, first
create your model (often done using the GUI in ACI-i). Next log into
ACI-b, and submit your job to the scheduler. For information on
submitting a job to ACI-b, see `section
7 <https://www.icds.psu.edu/computing-services/ics-aci-user-guide/#07-00-running-jobs-on-aci-b>`__.

An example of a PBS script to submit a COMSOL job:

.. raw:: html

   <pre class="script">#!/bin/bash

   #PBS -l nodes=1:ppn=4

   #PBS -l walltime=12:00:00

   #PBS -A open

   #PBS -o ComsolPBS.output

   #PBS -e ComsolPBS.error

   #PBS -m abe

   #PBS -M abc1234@psu.edu

   #PBS -n myComsolJob

   # Get started

   echo " "

   echo "Job started on ‘hostname‘ at ‘date‘"

   echo " "

   # Load in Comsol

   module purge

   module load comsol

   # Go to the correct place

   cd $PBS_O_WORKDIR

   # Run the job itself

   comsol batch -inputfile inputFile.mph -outputfile /path/to/output/outputFileName.mph -batchlog log.txt

   # Finish up

   echo " "

   echo "Job Ended at ‘date‘"

   echo " "

   </pre>

More information on options used for submitting comsol jobs using the
command line can be found by typing the commands:

.. raw:: html

   <pre>module load comsol
   comsol -h
   </pre>

9.3.2 Julia
'''''''''''

Julia is a high-level, high-performance dynamic programming language for
numerical computing. It provides a sophisticated compiler, distributed
parallel execution, numerical accuracy, and an extensive mathematical
function library. Julia’s Base library, largely written in Julia itself,
also integrates mature, best-of-breed open source C and Fortran
libraries for linear algebra, random number generation, signal
processing, and string processing.

The system Julia module is compiled with the GCC compiler. Using Julia
requires the gcc module to be loaded:

.. raw:: html

   <pre>$ module load gcc
   $ module load julia
   $ julia
   </pre>

Example Julia Code:

.. raw:: html

   <pre class="script">Pkg.add("Winston")

   using Winston

   # optionally call figure prior to plotting to set the size

   figure(width=600, height=400)

   # plot some data

   pl = plot(cumsum(rand(500) .- 0.5), "r", cumsum(rand(500) .- 0.5), "b")

   # display the plot (not done automatically!)

   display(pl)

   # by default display will not wait and the plot will vanish as soon as it appears

   # using readline is a blunt wait to allow the user to choose when to continue

   # println("Press enter to continue: ")

   # readline(STDIN)

   # save the current figure

   savefig("winston.svg")

   # .eps, .pdf, & .png are also supported

   # we used svg here because it respects the width and height specified above

   </pre>

An example PBS submission script for a julia simulation can be found:

.. raw:: html

   <pre class="script">#!/bin/bash

   #PBS -l procs=1

   #PBS -l walltime=240:00:00

   #PBS -l pmem=1000mb

   #PBS -n jobName

   #PBS -m ea

   #PBS -M PSU1234@psu.edu

   #PBS -j oe

   # Get started

   echo " "

   echo "Job started on ‘hostname‘ at ‘date‘"echo " "

   module load gcc

   module load julia

   cd $PBS_O_WORKDIR

   julia jobName.ji

   # Finish up

   echo " "

   echo "Job Ended at ‘date‘"

   echo " "

   </pre>

9.3.3 Matlab
''''''''''''

Matlab is a widely used programming environment and language. The GUI
can be accessed on ACI-i using the following commands:

.. raw:: html

   <pre>module load matlab
   matlab
   </pre>

Matlab can also be run in batch mode, either on the command line or
submitted as a job. Jobs run in batch mode must have an \*.m file. An
example that writes a random matrix as a .csv file:

.. raw:: html

   <pre class="script">%This Matlab script makes a random matrix and outputs a csv file of it.

   %This was made as a simple example to demostrate how to submit batch Matlab

   %codes

   %Created by i-ASK at ICDS of Penn State

   % June 27, 2017

   %% Create Random Matrix

   RandomMatrix = rand(5);

   %% Export csv file

   csvwrite(’output.csv’,RandomMatrix)

   </pre>

This can be saved as Example.m and submitted to ACI-b using the
following submission script:

.. raw:: html

   <pre class="script">#!/bin/bash

   #PBS -S /bin/bash

   #PBS -l nodes=1:ppn=1,walltime=00:05:00

   #PBS -N MyJobName

   #PBS -e error.txt

   #PBS -o output.txt

   #PBS -j oe

   #PBS -A open

   #PBS -m abe

   #PBS -M abc1234@psu.edu

   # Get started

   echo " "

   echo "Job started on ‘hostname‘ at ‘date‘"

   echo " "

   # Load in matlab

   module purge

   module load matlab

   # Run the job itself

   matlab -nodisplay -nosplash -r Example > logfile.matlabExample

   # Finish up

   echo " "

   echo "Job Ended at ‘date‘"

   echo " "

   </pre>

For more information about Matlab, please refer to the `Matlab
website <https://www.mathworks.com/products/matlab.html>`__.

9.3.4 Mathematica
'''''''''''''''''

Mathematica builds in unprecedentedly powerful algorithms across all
areas many of them created at Wolfram using unique development
methodologies and the unique capabilities of the Wolfram Alpha.
Mathematica is built to provide industrial-strength capabilities with
robust, efficient algorithms across all areas, capable of handling
large-scale problems, with parallelism, GPU computing, and more .
Mathematica provides a progressively higher-level environment in which
as much as possible is automated so you can work as efficiently as
possible.

The Mathematica module can be loaded with the command

.. raw:: html

   <pre>module load mathematica</pre>

A sample Mathematica code for printing random numbers into a text file:

.. raw:: html

   <pre class="script">Accumulate[RandomReal[{-1, 1}, 1000]]>>"output.txt"

   Quit [ ]

   </pre>

More examples of Mathematica code can be found
`here. <https://www.wolfram.com/language/gallery/>`__

Sample Shell script for Batch System

.. raw:: html

   <pre class="script">

#!/bin/bash

#PBS -N jobname

#PBS -l nodes=1:ppn= 1

#PBS -l mem=2gb,walltime=00:10:00

#PBS -A open

#PBS -o samplePBS.output

#PBS -e samplePBS.error

Get started
===========

echo " "

echo “Job started on ‘hostname‘ at ‘date‘”

echo " "

Load in Mathematica
===================

module purge

module load mathematica

Go to the correct place
=======================

cd $PBS_O_WORKDIR

Run the job itself
==================

math -noprompt -run ’<<samplecode.nb’

Finish up
=========

echo " "

echo “Job Ended at ‘date‘”

echo " "

.. raw:: html

   </pre>

An additional PBS submission script sample for Mathematica is given
here:

.. raw:: html

   <pre class="script">

#!/bin/bash

#PBS -l nodes=1:ppn=1

#PBS -l walltime=5:00

#PBS -A open

#PBS -o MathematicaPBS.output

#PBS -e MathematicaPBS.error

.. _get-started-1:

Get started
===========

echo " "

echo “Job started on ‘hostname‘ at ‘date‘”

echo " "

.. _load-in-mathematica-1:

Load in Mathematica
===================

module purge

module load mathematica

.. _go-to-the-correct-place-1:

Go to the correct place
=======================

cd $PBS_O_WORKDIR

.. _run-the-job-itself-1:

Run the job itself
==================

math -noprompt -run ’<<input.m’

.. _finish-up-1:

Finish up
=========

echo " "

echo “Job Ended at ‘date‘”

echo "

.. raw:: html

   </pre>

9.3.5 Stata
'''''''''''

Stata is a powerful statistical package with smart data-management
facilities, a wide array of up-to-date statistical techniques, and an
excellent system for producing publication-quality graphs. It is widely
used by many businesses and academic institutions especially in the
fields of economics, sociology, political science, biomedicine and
epidemiology. Stata is available for Windows, Linux/Unix, and Mac
computers. There are four versions of Stata as follows:

-  Stata/MP for multiprocessor computers (including dual-core and
   multicore processors). Stata/MP is licensed based on the maximum
   number of cores than an individual job can use. RCC licenses
   Stata/MP16, which can run on up to 16 cores.
-  Stata/SE for large databases
-  Stata/IC which is the standard version
-  Small Stata which is a smaller, student version of educational
   purchase only.

For parallel processing in Stata you must use stata-mp at the bottom of
your PBS script. You must also indicate the number of processors (up to
16) in the PBS script as well as your do file. As a line in your do file
be sure to include ”set processors n”, where n = the number of
processors and should be the same as the number in your PBS script. An
example PBS script is below where the number of processors is set to 8.

Setup:

In Linux, load the module with the following command before you start
working with Stata:

.. raw:: html

   <pre>module load stata</pre>

Note that this command will load the current version. Other available
versions can be checked by following command:

.. raw:: html

   <pre>module avail stata</pre>

Usage To start Stata , type:

.. raw:: html

   <pre>stata-mp</pre>

Use only ACI-i for interactive jobs. If you are remotely connecting to
our systems via Open OnDemand, we recommend using the GUI version of
Stata:

.. raw:: html

   <pre>xstata-mp</pre>

Batch usage: Sample PBS script is given below:

.. raw:: html

   <pre class="script">#!/bin/bash

   #PBS -l nodes=1:ppn=1

   #PBS -l walltime=00:15:00

   #PBS -A open

   #PBS -n jobName

   #PBS -M user123@psu.edu

   #PBS -m abe

   #PBS -j oe

   # Get started

   echo " "

   echo "Job started on ‘hostname‘ at ‘date‘"

   echo " "

   # Load in Stata

   module purge

   module load stata

   # Go to the correct place

   cd $PBS_O_WORKDIR

   # Run the job itself

   stata -b do filename

   # Finish up

   echo " "

   echo "Job Ended at ‘date‘"

   echo " "

   </pre>

You can use stata-mp by substituting the stata command with the
following:

.. raw:: html

   <pre>stata-mp -b do jobName.do</pre>

9.3.6 Python
''''''''''''

Python is a multi-use programming language used in a wide variety of
fields. It can be run in batch mode on ACI-i or used in submitted jobs
on ACI-b.

An example python script, named jobName.py:

.. raw:: html

   <pre class="script">import sys

   jobName = [Hello, World]

   for i in jobName:

   print i

   sys.exit(0)

   #end of jobName.py

   </pre>

This script can be submitted as a job on ACI-b with the following
script:

.. raw:: html

   <pre class="script">#!/bin/bash -l

   #PBS N jobName

   #PBS l nodes=1:ppn=12

   #PBS l walltime=00:05:00

   #PBS j oe

   #PBS -M abc123@psu.edu

   # Get started

   echo " "

   echo "Job started on ‘hostname‘ at ‘date‘"

   echo " "

   #load in python

   module purge

   module load python/2.7.1

   #go to the correct work directory

   cd $PBS_O_WORKDIR

   python jobName.py

   # Finish up

   echo " "

   echo "Job Ended at ‘date‘"

   echo " "

   </pre>

For more information, please feel free to refer to the `Python
website <https://www.python.org/>`__.

An excellent resource for various plotting methods found within python
can be found at the `matplotlib
gallery. <https://matplotlib.org/gallery.html>`__

9.3.7 Singularity
'''''''''''''''''

Singularity is a *container* system developed for use on
high-performance computing clusters. Container computing allows the
creation of a virtual-machine-like environment, which gives the user
access to different configurations of software for use on clusters.

Using Singularity to install a container on Roar can help users:

-  avoid dependence challenges
-  perform the same expected behavior on local and remote systems
-  easily move containers to new locations

This may help if you need to run a container without having sudo access,
but keep in mind that the container must integrate seamlessly into the
existing destination infrastructure.

*8.3.7.1 Getting Started with Using Singularity*

Before getting started with using Singularity on Roar, you will need to
install Singularity on a system for which you have root access.
`Singularity’s official user guide <https://www.sylabs.io/docs/>`__
provides instructions for doing this. Roar uses version 2.6.0 of
Singularity.

You may also obtain help in ACI-b like so:

.. raw:: html

   <pre class="script">[cjb47@comp-sc-0157 ~]$ singularity help
   USAGE: singularity [global options...] <command></command> [command options...] ...
   GLOBAL OPTIONS:
   -d|--debug Print debugging information
   -h|--help Display usage summary
   -s|--silent Only print errors
   -q|--quiet Suppress all normal output
   --version Show application version
   -v|--verbose Increase verbosity +1
   -x|--sh-debug Print shell wrapper debugging information
   GENERAL COMMANDS:
   help Show additional help for a command or container
   selftest Run some self tests for singularity install
   CONTAINER USAGE COMMANDS:
   exec Execute a command within container
   run Launch a runscript within container
   shell Run a Bourne shell within container
   test Launch a testscript within container
   CONTAINER MANAGEMENT COMMANDS:
   apps List available apps within a container
   bootstrap *Deprecated* use build instead
   build Build a new Singularity container
   check Perform container lint checks
   inspect Display container's metadata
   mount Mount a Singularity container image
   pull Pull a Singularity/Docker container to $PWD
   COMMAND GROUPS:
   image Container image command group
   instance Persistent instance command group
   CONTAINER USAGE OPTIONS:
   see singularity help <command></command>
   For any additional help or support visit the Singularity
   website: https://www.sylabs.io</pre>

*9.3.7.2 Images supported*

Singularity supports many types of containers, which are also known as
images. These include:

========== ==============================================
Image Type Description
========== ==============================================
simg       standard image
directory  Unix Directory containing root container image
tar.gz     Gzip compressed tar archive
tar.bx2    Bzip2 compressed tar archive
tar        uncompressed tar archive
cpio.gz    Gzip compressed CPIO archive
cpio       Uncompressed CPIO archive
========== ==============================================

Standard image and directory are the most commonly used formats. The
others tend to be archive of the directory format that are decompressed
on the fly.

| *Note: Docker Integration*
| Singularity supports Docker natively and directly. This means that
  nearly all Docker images can be used directly as long as the required
  functionality does not require root access; however, most applications
  do not require this. We provide an example in the next section,
  Obtaining pre-built images.

*9.3.7.3 Obtaining Pre-built Images*

Images built by others users, sometimes the developers of the desired
software itself, are among the best choices for a base image and, in
many cases, may be all a researcher needs to do to have an image that
gives the desired outcome.

Here is a common-example, the Docker image, lolcow.

.. raw:: html

   <pre class="script">[cjb47@comp-sc-0161 ~]$ singularity run docker://godlovedc/lolcow
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   Docker image path: index.docker.io/godlovedc/lolcow:latest
   Cache folder set to /storage/home/c/cjb47/.singularity/docker
   [1/1] |===================================| 100.0%
   Creating container runtime...
   Exploding layer:
   ˓→sha256:9fb6c798fa41e509b58bccc5c29654c3ff4648b608f5daa67c1aab6a7d02c118.tar.gz
   Exploding layer:
   ˓→sha256:3b61febd4aefe982e0cb9c696d415137384d1a01052b50a85aae46439e15e49a.tar.gz
   Exploding layer:
   ˓→sha256:9d99b9777eb02b8943c0e72d7a7baec5c782f8fd976825c9d3fb48b3101aacc2.tar.gz
   Exploding layer:
   ˓→sha256:d010c8cf75d7eb5d2504d5ffa0d19696e8d745a457dd8d28ec6dd41d3763617e.tar.gz
   Exploding layer:
   ˓→sha256:7fac07fb303e0589b9c23e6f49d5dc1ff9d6f3c8c88cabe768b430bdb47f03a9.tar.gz
   Exploding layer:
   ˓→sha256:8e860504ff1ee5dc7953672d128ce1e4aa4d8e3716eb39fe710b849c64b20945.tar.gz
   Exploding layer:
   ˓→sha256:736a219344fbca3099ce5bd1d2dbfea74b22b830bac0e85ecca812c2983390cd.tar.gz
   WARNING: Non existent bind point (directory) in container: '/storage/home'
   WARNING: Non existent bind point (directory) in container: '/storage/work'
   WARNING: Non existent bind point (directory) in container: '/gpfs/scratch'
   WARNING: Non existent bind point (directory) in container: '/gpfs/group'
   WARNING: Non existent bind point (directory) in container: '/var/spool/torque'
   WARNING: Could not chdir to home: /storage/home/cjb47
   ________________________________________
   / Tonight you will pay the wages of sin; \
   \ Don't forget to leave a tip. /
   ----------------------------------------
   \   ^__^
   \   (oo)\_______
       (__)\       )\/\
           ||----w |
           ||     ||
   </pre>

This example presents problems in certain cases, because the image does
not have access to the data on the Roar system:

.. raw:: html

   <pre class="script">[cjb47@comp-sc-0185 singularity]$ singularity shell docker://godlovedc/lolcow
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   Docker image path: index.docker.io/godlovedc/lolcow:latest
   Cache folder set to /storage/home/c/cjb47/.singularity/docker
   Creating container runtime...
   Exploding layer:
   ˓→sha256:9fb6c798fa41e509b58bccc5c29654c3ff4648b608f5daa67c1aab6a7d02c118.tar.gz
   Exploding layer:
   ˓→sha256:3b61febd4aefe982e0cb9c696d415137384d1a01052b50a85aae46439e15e49a.tar.gz
   Exploding layer:
   ˓→sha256:9d99b9777eb02b8943c0e72d7a7baec5c782f8fd976825c9d3fb48b3101aacc2.tar.gz
   Exploding layer:
   ˓→sha256:d010c8cf75d7eb5d2504d5ffa0d19696e8d745a457dd8d28ec6dd41d3763617e.tar.gz
   Exploding layer:
   ˓→sha256:7fac07fb303e0589b9c23e6f49d5dc1ff9d6f3c8c88cabe768b430bdb47f03a9.tar.gz
   Exploding layer:
   ˓→sha256:8e860504ff1ee5dc7953672d128ce1e4aa4d8e3716eb39fe710b849c64b20945.tar.gz
   Exploding layer:
   ˓→sha256:736a219344fbca3099ce5bd1d2dbfea74b22b830bac0e85ecca812c2983390cd.tar.gz
   WARNING: Non existent bind point (directory) in container: '/storage/home'
   WARNING: Non existent bind point (directory) in container: '/storage/work'
   WARNING: Non existent bind point (directory) in container: '/gpfs/scratch'
   WARNING: Non existent bind point (directory) in container: '/gpfs/group'
   WARNING: Non existent bind point (directory) in container: '/var/spool/torque'
   WARNING: Could not chdir to home: /storage/home/cjb47
   Singularity: Invoking an interactive shell within container...
   Singularity lolcow:/> cd ~
   bash: cd: /storage/home/cjb47: No such file or directory
   </pre>

We can note the first issue, the non-existent bind paths. For this type
of image, add the bind paths by slightly modifying the images. This can
be done by writing a simple set of instructions, which are used to
create an image. This set of instructions is called a recipe, in
Singularity terminology.

*9.3.7.4 Handling the Bind Paths on Roar*

In order to handle the bind paths, it is very helpful to start with a
recipe to set the data paths, even if the image is mostly a prepared
image from another source. We will take a look at how to do this, and
then discuss the building process in more detail.

We can also start with a recipe and add the correct binding paths for
ACI-b. Here is a simple example to handle the bind points using the
lolcow image.

.. raw:: html

   <pre class="script">BOOTSTRAP: docker
   FROM: godlovedc/lolcow
   %post
   #ACI mappings so you can access your files.
   mkdir -p /storage/home
   mkdir -p /storage/work
   mkdir -p /gpfs/group
   mkdir -p /gpfs/scratch
   mkdir -p /var/spool/torque
   </pre>

We build the image in an environment where we have sudo access (not
Roar):

.. raw:: html

   <pre class="script">[cjb47@localhost simple_bind]$ sudo singularity build ./lolcow.simg ./lolcow.recipe
   Building into existing container: ./lolcow.simg
   Using container recipe deffile: ./lolcow.recipe
   Sanitizing environment
   Adding base Singularity environment to container
   Running post scriptlet
   + mkdir -p /storage/home
   + mkdir -p /storage/work
   + mkdir -p /gpfs/group
   + mkdir -p /gpfs/scratch
   + mkdir -p /var/spool/torque
   Found an existing definition file
   Adding a bootstrap_history directory
   Finalizing Singularity container
   Calculating final size for metadata...
   Skipping checks
   Building Singularity image...
   Singularity container built: ./lolcow.simg
   Cleaning up...
   </pre>

Next, transfer the image to Roar using scp, and run it:

.. raw:: html

   <pre class="script">[cjb47@comp-sc-0185 images]$ singularity run ./lolcow.simg
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   _________________________________________
   / The Priest's grey nimbus in a niche \
   | where he dressed discreetly. I will not |
   | sleep here tonight. Home also I cannot |
   | go. |
   | |
   | A voice, sweetened and sustained, |
   | called to him from the sea. Turning the |
   | curve he waved his hand. A sleek brown |
   | head, a seal's, far out on the water, |
   | round. Usurper. |
   | |
   \ -- James Joyce, "Ulysses" /
   -----------------------------------------
   \   ^__^
   \   (oo)\_______
       (__)\       )\/\
           ||----w |
           ||     ||
   </pre>

Note that we are now able to access our data on the local Roar
locations.

.. raw:: html

   <pre class="script">[cjb47@comp-sc-0185 images]$ singularity shell ./lolcow.simg
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   Singularity: Invoking an interactive shell within container...
   Singularity lolcow.simg:/gpfs/group/dml129/default/cjb47/singularity/images> cd ~
   Singularity lolcow.simg:~> pwd
   /storage/home/cjb47
   </pre>

9.3.7.5 Ways of using Singularity containers
''''''''''''''''''''''''''''''''''''''''''''

Once a container has been built and is placed on Roar, you can use it in
a variety of ways. Here, we explain a few ways, including:

-  ACI-b interactive sessions
-  ACI-n batch sessions
-  Interactive shells
-  Executing commands
-  Running a container
-  Working with files

*ACI-b Interactive Sessions:*

You can start an interactive sessions with X-forwarding using the
following command:

(script: qsub -l walltime=04:00:00 -l nodes=1:ppn=4 -A open -I -X)O

**Warning:** Do not run interactive sessions on the log-in (head) nodes.
These nodes are shared among all users and can quickly be rendered
unusable by computationally intensive jobs on the sessions. Use of the
head nodes to perform computationally demanding tasks can lead to the
programs being terminated, or deactivation of the user’s access to Roar.

*ACI-b Batch Sessions:*

Here are a few examples that will run an application or command
non-interactively in a PBS job file.

.. raw:: html

   <pre class="script">#!/bin/bash
   #PBS -N Lammps-singularity
   #PBS -A open
   #PBS -l walltime=04:00:00
   #PBS -l nodes=2:ppn=20
   #PBS -j oe
   module load gcc/5.3.1 mpich/3.2
   cd $PBS_O_WORKDIR
   mpirun --hostfile $PBS_NODEFILE --np 40 singularity run /path/to/lammps_mpi.simg   in.
   ˓→friction \
   > out.friction
   </pre>

*Interactive Shells:*

If you need to use many interactive tools or applications, you may want
to start an interactive shell. Use the following command to do this:

.. raw:: html

   <pre class="script">[cjb47@comp-bc-0226 images]$ cat /etc/issue
   Red Hat Enterprise Linux Server release 6.10 (Santiago)
   Kernel \r on an \m
   [cjb47@comp-bc-0226 images]$ singularity shell ubuntu_aci.simg
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   Singularity: Invoking an interactive shell within container...
   Singularity ubuntu_aci.simg:/gpfs/group/dml129/default/cjb47/singularity/images> cat /
   ˓→etc/issue
   Ubuntu 16.04.5 LTS \n \l
   </pre>

You will be able to interact with directories that have been bound.

*Executing Commands:*

In some cases, you may only want to run a single command from within the
container. The following is an example of this:

.. raw:: html

   <pre class="script">[cjb47@comp-bc-0226 images]$ R
   R version 3.5.0 (2018-04-23) -- "Joy in Playing"
   Copyright (C) 2018 The R Foundation for Statistical Computing
   Platform: x86_64-redhat-linux-gnu (64-bit)
   R is free software and comes with ABSOLUTELY NO WARRANTY.
   You are welcome to redistribute it under certain conditions.
   Type 'license()' or 'licence()' for distribution details.
   R is a collaborative project with many contributors.
   Type 'contributors()' for more information and
   'citation()' on how to cite R or R packages in publications.
   Type 'demo()' for some demos, 'help()' for on-line help, or
   'help.start()' for an HTML browser interface to help.
   Type 'q()' to quit R.
   > q()
   Save workspace image? [y/n/c]: n
   [cjb47@comp-bc-0226 images]$ singularity run shub://jekriske/r-base:3.4.4 R
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   Progress |===================================| 100.0%
   WARNING: Non existent mountpoint (directory) in container: '/var/singularity/mnt/
   ˓→final/storage/home'
   WARNING: Non existent mountpoint (directory) in container: '/var/singularity/mnt/
   ˓→final/storage/work'
   WARNING: Non existent mountpoint (directory) in container: '/var/singularity/mnt/
   ˓→final/gpfs/scratch'
   WARNING: Non existent mountpoint (directory) in container: '/var/singularity/mnt/
   ˓→final/gpfs/group'
   WARNING: Non existent mountpoint (directory) in container: '/var/singularity/mnt/
   ˓→final/var/spool/torque'
   WARNING: Could not chdir to home: /storage/home/cjb47
   ARGUMENT 'R' __ignored__
   R version 3.4.4 (2018-03-15) -- "Someone to Lean On"
   Copyright (C) 2018 The R Foundation for Statistical Computing
   Platform: x86_64-pc-linux-gnu (64-bit)
   R is free software and comes with ABSOLUTELY NO WARRANTY.
   You are welcome to redistribute it under certain conditions.
   Type 'license()' or 'licence()' for distribution details.
   Natural language support but running in an English locale
   R is a collaborative project with many contributors.
   Type 'contributors()' for more information and
   'citation()' on how to cite R or R packages in publications.
   Type 'demo()' for some demos, 'help()' for on-line help, or
   'help.start()' for an HTML browser interface to help.
   Type 'q()' to quit R.
   > q()
   Save workspace image? [y/n/c]: n
   </pre>

*Running a Container:*

Some containers may have one or more runscripts, which allow a user to
define a set of actions a container will run when it is called. For
example:

.. raw:: html

   <pre class="script">[cjb47@comp-bc-0226 images]$ singularity run ./hello-world-aci.simg
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   Hello there cjb47, from ICDS
   </pre>

A container may have multiple runscripts; in Singularity terminology,
this is known as an “application.” Here is an example, including
instructions for interacting with applications:

.. raw:: html

   <pre class="script">[cjb47@comp-sc-0120 images]$ singularity apps ./multiapps-aci.simg
   cowsay
   fortune
   lolcat
   [cjb47@comp-sc-0120 images]$ singularity run --app fortune ./multiapps-aci.simg -a
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   FORTUNE PROVIDES QUESTIONS FOR THE GREAT ANSWERS: #19
   A: To be or not to be.
   Q: What is the square root of 4b^2?
   [cjb47@comp-sc-0120 images]$ echo "Hello from lolcat" > file
   [cjb47@comp-sc-0120 images]$ singularity run --app lolcat ./multiapps-aci.simg file
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   Hello from lolcat
   </pre>

*Working with Files:*

As long as there are corresponding binding points, you will be able to
reach files on the host from within the container. Since Roar has user
storage in non-standard locations (compared to distribution default),
you will need to add the appropriate locations to a recipe.

In the following example, we need binding for ACI-b:

.. raw:: html

   <pre class="script">%post
   #ACI mappings so you can access your files.
   mkdir -p /storage/home
   mkdir -p /storage/work
   mkdir -p /gpfs/group
   mkdir -p /gpfs/scratch
   mkdir -p /var/spool/torque
   </pre>

9.3.7.6 More information on building Singularity containers
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

The official `Singularity user
guide <https://www.sylabs.io/guides/2.6/user-guide/>`__ has additional
information and examples related to building and using Singularity
containers.

Following are several other use cases:

-  Building containers with GUI support
-  Building an image with MPI support
-  Images with GPU support
-  Running Services
-  Using sandbox and writable images

*Building Containers with GUI Support*

A Singularity container can contain a GUI system so that the user can
run a GUI application that may not easily be installed on Roar. Here is
a simple example of a recipe that has a GUI available:

.. raw:: html

   <pre class="script">Bootstrap: docker
   From: centos:centos7
   %post
   yum -y upgrade
   yum -y groupinstall "X Window System"
   rpm --import https://packages.microsoft.com/keys/microsoft.asc
   echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/
   ˓→yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/
   ˓→microsoft.asc" > /etc/yum.repos.d/vscode.repo
   yum install -y nano emacs vim gedit kate nedit kwrite jed code
   yum -y install which xorg-x11-fonts-Type1 liberation-sans-fonts
   yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
   yum -y install geany geany-plugins*
   mkdir -p /storage/home
   mkdir -p /storage/work
   mkdir -p /gpfs/group
   mkdir -p /gpfs/scratch
   mkdir -p /var/spool/torque
   mkdir -p /run/user/1000/dconf
   touch /run/user/1000/dconf/user
   %runscript
   </pre>

Here is a screenshot of an editor running within that container on an
ACI-b compute node:

|image0|

*Building an Image with MPI Support*

Many HPC applications require the use of MPI. Singularity supports this;
however, there are requirements for this:

-  Install InfiniBand libraries in the container
-  Make the MPI version available to the container, which may be
   accomplished by setting a bind path to the MPI location
-  The application must be linked the proper version of MPI

Here is an example of the MPI build file:

.. raw:: html

   <pre class="script">BootStrap: yum
   OSVersion: 7
   MirrorURL: http://mirror.centos.org/centos-%{OSVERSION}/%{OSVERSION}/os/$basearch/
   Include: yum
   %setup
   cd $SINGULARITY_ROOTFS/opt
   wget http://www.mpich.org/static/downloads/3.2/mpich-3.2.tar.gz
   wget http://lammps.sandia.gov/tars/lammps-stable.tar.gz
   %post
   yum -y groupinstall "Development Tools"
   mkdir -p /opt/mpich
   cd /opt/mpich
   tar xf ../mpich-3.2.tar.gz --strip-components 1
   ./configure --prefix=/usr/local |& tee log.configure
   make -j |& tee log.make
   make install |& tee log.make_install
   mkdir -p /opt/lammps
   cd /opt/lammps
   tar xf ../lammps-stable.tar.gz --strip-components 1
   cd src
   make yes-granular |& tee log.make_yes_granular
   make -j mpi |& tee log.make_mpi
   #ACI mappings so you can access your files.
   mkdir -p /storage/home
   mkdir -p /storage/work
   mkdir -p /gpfs/group
   mkdir -p /gpfs/scratch
   mkdir -p /var/spool/torque
   %runscript
   /opt/lammps/src/lmp_mpi "$@"
   </pre>

Here is an example of an MPI run:

.. raw:: html

   <pre class="script">[cjb47@comp-sc-0174 images]$ module load gcc/5.3.1 mpich/3.2
   [cjb47@comp-sc-0174 images]$ mpirun --hostfile $PBS_NODEFILE -np 8 singularity run ./
   ˓→lammps_mpi.simg  in.friction
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   ** NOTE: Singularity is in a testing phase on ACI-b and is currently unsupported.
   LAMMPS (22 Aug 2018)
   Lattice spacing in x,y,z = 1.1327 1.96189 1.1327
   Created orthogonal box = (0 0 -0.283174) to (56.6348 43.1615 0.283174)
   4 by 2 by 1 MPI processor grid
   Created 750 atoms
   Time spent = 0.00195265 secs
   Created 750 atoms
   Time spent = 0.00053978 secs
   Created 112 atoms
   Time spent = 0.000246286 secs
   Created 112 atoms
   Time spent = 0.0002985 secs
   750 atoms in group lo
   862 atoms in group lo
   750 atoms in group hi
   862 atoms in group hi
   150 atoms in group lo-fixed
   150 atoms in group hi-fixed
   300 atoms in group boundary
   1424 atoms in group mobile
   Setting atom values ...
   150 settings made for type
   Setting atom values ...
   150 settings made for type
   WARNING: Temperature for thermo pressure is not for group all (../thermo.cpp:488)
   Neighbor list info ...
   update every 1 steps, delay 5 steps, check yes
   max neighbors/atom: 2000, page size: 100000
   master list distance cutoff = 2.8
   ghost atom cutoff = 2.8
   binsize = 1.4, bins = 41 31 1
   1 neighbor lists, perpetual/occasional/extra = 1 0 0
   (1) pair lj/cut, perpetual
   attributes: half, newton on
   pair build: half/bin/atomonly/newton
   stencil: half/bin/2d/newton
   bin: standard
   Setting up Verlet run ...
   Unit style : lj
   Current step : 0
   Time step : 0.0025
   Per MPI rank memory allocation (min/avg/max) = 3.048 | 3.049 | 3.049 Mbytes
   Step Temp E_pair E_mol TotEng Press Volume
   0 0.1 -3.1333672 0 -3.0920969 -1.1437663 2444.9333
   1000 0.1 -3.0917089 0 -3.0504386 -0.023690937 2444.9333
   2000 0.082122114 -3.0852042 0 -3.0513121 -0.43261548 2444.9333
   3000 0.081076017 -3.0813279 0 -3.0478675 -0.34285337 2444.9333
   4000 0.094734274 -3.0722764 0 -3.0331792 -0.31676394 2444.9333
   5000 0.11433917 -3.0594274 0 -3.0122393 -0.14791034 2444.9333
   6000 0.11055427 -3.046338 0 -3.0007119 -0.22376263 2444.9333
   7000 0.1 -3.045677 0 -3.0044067 -0.42807494 2444.9333
   8000 0.11471279 -3.0383911 0 -2.9910488 -0.30901046 2444.9333
   9000 0.11181441 -3.037818 0 -2.9916719 -0.41346773 2444.9333
   10000 0.10709722 -3.0390765 0 -2.9948772 -0.27785942 2444.9333
   11000 0.1 -3.0404147 0 -2.9991444 -0.50482354 2444.9333
   12000 0.11767118 -3.0483134 0 -2.9997502 -0.12862642 2444.9333
   13000 0.11773859 -3.0569926 0 -3.0084016 -0.36892682 2444.9333
   14000 0.11272521 -3.0514207 0 -3.0048987 -0.36445405 2444.9333
   15000 0.10522749 -3.0506428 0 -3.0072151 -0.35624388 2444.9333
   16000 0.11015277 -3.0509982 0 -3.0055378 -0.19177436 2444.9333
   17000 0.1081148 -3.0478773 0 -3.003258 -0.3475267 2444.9333
   18000 0.11109139 -3.0476586 0 -3.0018109 -0.33148148 2444.9333
   19000 0.10911522 -3.0523013 0 -3.0072692 -0.25645655 2444.9333
   20000 0.11656944 -3.0534574 0 -3.0053488 -0.33684091 2444.9333
   Loop time of 6.56253 on 8 procs for 20000 steps with 1724 atoms
   Performance: 658283.185 tau/day, 3047.607 timesteps/s
   74.8% CPU use with 8 MPI tasks x no OpenMP threads
   MPI task timing breakdown:
   Section | min time | avg time | max time |%varavg| %total
   ---------------------------------------------------------------
   Pair | 0.4896 | 0.57526 | 0.75825 | 10.7 | 8.77
   Neigh | 0.029521 | 0.03774 | 0.052896 | 4.3 | 0.58
   Comm | 3.6847 | 4.1707 | 5.064 | 25.3 | 63.55
   Output | 0.0028827 | 0.0031309 | 0.0033143 | 0.3 | 0.05
   Modify | 0.076676 | 0.083922 | 0.09419 | 1.8 | 1.28
   Other | | 1.692 | | | 25.78
   Nlocal: 215.5 ave 286 max 189 min
   Histogram: 5 1 0 0 0 0 0 0 1 1
   Nghost: 97.875 ave 131 max 77 min
   Histogram: 2 1 1 1 1 0 0 0 1 1
   Neighs: 1802 ave 2442 max 1569 min
   Histogram: 5 1 0 0 0 0 0 0 1 1
   Total # of neighbors = 14416
   Ave neighs/atom = 8.36195
   Neighbor list builds = 720
   Dangerous builds = 0
   Total wall time: 0:00:06
   </pre>

*Images with GPU Support*

You can build a Singularity image with GPU support or find a pre-built
one. You will need to make sure the version of CUDA that is to be used
(i.e., the version of the CUDA that will be in the environment, check
GPU documentation for more information) matches that of the image you
plan to use. The `Official Singularity User
Guide <http://singularity.lbl.gov/docs-instances>`__ has more details.

Note that many services require sudo access and thus cannot be run on
Roar.

*Running Services*

In some cases, a piece of software, such as database or web server, is
meant to be run in the background and accessed as a server. In some
cases, it is possible to run these as an instance.

*Using Sandbox and Writable Images*

| Recipes are the most reproducible method of preparing images, but you
  can use writable and sandbox images to build the image interactively.
  By default, all Singularity images are temporary, which means changes
  are not retained when the image is stopped (i.e., when
| the shell is exited, the command has completed running, or the
  instance is stopped by the ``instance.stop`` command).

10 Policies
~~~~~~~~~~~

By requesting a Roar user account, users acknowledge that they have read
and understood all Roar and applicable Pennsylvania State University
policies and agree to abide by said policies. All policies can be found
at our `policies
page <https://www.icds.psu.edu/computing-services/icds-aci-policies/>`__.

10.1 Authentication and Access Control
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This policy serves to manage the lifecycle of accounts created under the
current state and configuration of Roar. It specifies criteria for
creating a user account, using an account, and termination of a user
account.

10.2 Data Protection and Retention
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This policy outlines the protection of data that is created, collected
or manipulated by personnel that fall within the scope of Roar and
applies to any person who uses Roar resources or handles data managed by
Roar. It specifies data retention policies and resources, as well as the
responsibilities of the principal investigator, the University, and
Roar.

10.3 Software Acceptable Use
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This policy explains how software is introduced, installed, and
maintained on the Roar computer system. The policy details how users can
install their own software in their user or group spaces, as well as how
ICDS will regularly update the Roar software stack. Information on how
to request new software for the Roar software stack is included. The
policy also discusses who is responsible for licensing and usage
agreements in various circumstances, and the rights that ICDS reserves
to make changes to installed software in order to keep Roar systems
safe, up-to-date, and in compliance with University and government
regulations.

10.4 SLA Terms and Conditions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This terms and conditions document outlines the basic provisions that
guide the working relationships between researchers and Roar.

11 For Further Assistance
~~~~~~~~~~~~~~~~~~~~~~~~~

The `i-ASK Center <https://iask.aci.ics.psu.edu>`__ provides prompt,
expert assistance for any issues researchers might encounter on Roar and
is the point of contact for the ICDS technical staff. This help desk web
portal lets you submit and track tickets and features a helpful list of
FAQs. The i-ASK Center also provides timely system alerts regarding
maintenance and other events that impact the system.

Table of Contents
~~~~~~~~~~~~~~~~~

-  `0 We’re Redesigning the Roar User
   Guide! <#0-were-redesigning-the-roar-user-guide>`__
-  `1 Introduction <#01-00-introduction>`__

   -  `1.1 What is Roar? <#01-01-icds-aci>`__
   -  `1.2 What does Roar do? <#01-02-icds-aci>`__
   -  `1.3 Our Mission <#01-03-mission>`__
   -  `1.4 Our Vision <#01-04-vision>`__

-  `2 Roar History <#02-00-ics-aci-history>`__
-  `3 System Overview <#03-00-system-overview>`__

   -  `3.1 ACI-b <#03-01-aci-b>`__
   -  `3.2 ACI-I <#03-02-aci>`__
   -  `3.3 Roar Open Queue <#03-03-aci-open-queue>`__
   -  `3.4 HPRC <#03-04-hprc>`__
   -  `3.5 Filesystems <#03-05-filesystems>`__
   -  `3.6 Data Manager <#03-06-data-manager>`__

-  `4 System Access <#04-00-system-access>`__

   -  `4.1 Sponsorship <#04-01-sponsorship>`__
   -  `4.2 Permissions to use
      Resources <#04-02-permissions-use-resources>`__
   -  `4.3 Getting an Account <#04-03-getting-account>`__

-  `5 Basics of the Roar Resources <#05-00-basics-aci-resources>`__

   -  `5.1 System Usage <#05-01-system-usage>`__
   -  `5.2 Module System <#05-02-module-system>`__
   -  `5.3 Connecting to ACI-b <#05-03-connecting-aci-b>`__
   -  `5.4 Connecting to ACI-i <#05-04-connecting-aci>`__

      -  `5.4.1 Open OnDemand <#05-041-open-ondemand>`__

   -  `5.5 Connecting to HPRC <#05-05-connecting-to-hprc>`__
   -  `5.6 Transferring Data to and from
      Roar <#05-06-transferring-data-aci>`__

-  `6 Application Development <#06-00-application-development>`__

   -  `6.1 Version Control <#06-01-version-control>`__
   -  `6.2 Basic Compilation <#06-02-basic-compilation>`__
   -  `6.3 Libraries <#06-03-libraries>`__

-  `7 Running Jobs on ACI-b <#07-00-running-jobs-on-aci-b>`__

   -  `7.1 Requesting Resources <#07-01-requesting-resources>`__
   -  `7.2 Interactive Compute Sessions on
      ACI-b <#07-02-interactive-compute-sessions-aci-b>`__
   -  `7.3 PBS Environmental
      Variables <#07-03-pbs-environmental-variables>`__
   -  `7.4 GReaT Allocations <#07-04-great-allocations>`__
   -  `7.5 ACI-b GPU nodes <#07-05-aci-b-gpu-nodes>`__

-  `8 Running Jobs on HPRC <#08-00-running-jobs-on-hprc>`__

   -  `8.1 Requesting Resources <#08-01-requesting-resources>`__

      -  `8.1.1 Sample HPRC Batch Submission
         Script <#08-012-sample-script>`__

   -  `8.2 Interactive Compute Sessions on
      HPRC <#08-02-interactive-compute-sessions-on-hprc>`__
   -  `8.3 Requesting a Custom Singularity Container on
      HPRC <#08-03-requesting-a-custom-singularity-container-on-hprc>`__
   -  `8.4 Specifying a Custom Bash Environment on
      HPRC <#08-04-specifying-a-custom-bash-environment-on-hprc>`__

-  `9 Software Stack <#09-00-software-stack>`__

   -  `9.1 User Stack <#09-01-user-stack>`__
   -  `9.2 System Stack <#09-02-system-stack>`__
   -  `9.3 System Stack
      Applications <#09-03-system-stack-applications>`__

-  `10 Policies <#10-00-policies>`__

   -  `10.1 Authentication and Access
      Control <#10-01-authentication-access-control>`__
   -  `10.2 Data Protection and
      Retention <#10-02-data-protection-retention>`__
   -  `10.3 Software Acceptable Use <#10-03-software-acceptable-use>`__
   -  `10.4 SLA Terms and Conditions <#10-04-sla-terms-conditions>`__

-  `11 For Further Assistance <#11-00-for-further-assistance>`__

`Back to Top ▲ <#jump-top>`__

|Penn State Institute for Computational and Data Sciences Logo|

| 224B Computer Building
| icds@psu.edu
| 814-867-1467

About

-  `Overview <https://www.icds.psu.edu/about/>`__
-  `Staff <https://www.icds.psu.edu/about/meet-the-icds-team/icds-staff/>`__
-  `Careers <https://www.icds.psu.edu/careers/>`__
-  `Sitemap <https://www.icds.psu.edu/sitemap/>`__

i-ASK Support Center

-  `Account
   Set-Up <https://www.icds.psu.edu/computing-services/account-setup/>`__
-  `Roar Supercomputer User
   Guide <https://www.icds.psu.edu/computing-services/roar-user-guide/>`__
-  `i-ASK Help
   Center <https://www.icds.psu.edu/computing-services/support/>`__
-  814-865-4275

Sign Up for ICDS Announcements

-  `Subscribe to Our Mailing List </subscribe>`__

Follow Us

-  ` <https://twitter.com/icds_psu>`__
-  ` <https://www.youtube.com/channel/UCnPq-88xAN4YeMbfD5_7Crg>`__
-  ` <https://www.facebook.com/PennStateICDS/>`__
-  ` <https://www.linkedin.com/company/penn-state-institute-for-computational-and-data-sciences>`__

`Penn State. <http://www.psu.edu/>`__ All rights reserved. `Privacy and
Legal Statements <http://www.psu.edu/ur/legal.html>`__

.. |image0| image:: https://www.icds.psu.edu/wp-content/uploads/2018/11/UsingSingularityonACI-screenshot-1024x999.jpg
.. |Penn State Institute for Computational and Data Sciences Logo| image:: https://www.icds.psu.edu/wp-content/themes/ics/assets/images/PSU_logo_white.png
   :target: /
