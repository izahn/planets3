Software Environments and Desktop Integrations for High Performance Computing
=============================================================================

:Author:        Ista Zahn
:Updated:       2021-03-03
:LifeCycle:     In development, "Beta"

This project provides software to install and configure environments 
for use in HPC clusters. If provides up-to-date open-source data science
stacks including Python, R, Octave, QGIS, and integrates other software (like
Matlab, Stata, SAS, etc.) that you already have installed. It integrates 
LSF with the GNOME 3 desktop to offer convenient application launchers and
utilities.

This `short video <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/userguide/html/video.html>`_
serves as an introduction to the project and will give you a sense of what it can do.

A `user guide <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/userguide/html>`_ 
is available, along with 
`dev-ops / implementation documentation <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/devops_docs/html/>`_.

Main Features
-------------

For DevOps / Sysadmins:

- `Reproducible and documented environment creation and configuration <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/devops_docs/html/devops.html>`_
  ("infrastructure as code").
- Robust and comprehensive open-source statistics and data science environments using the `conda package manager <https://docs.conda.io>`_.
- `Documented procedure for creating and releasing updated software environments <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/devops_docs/html/devops.html#updates-and-new-environments>`_
- Integration with existing Lmod modules and proprietary software already installed on your system. 

For users:

- `Graphical launchers <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/userguide/html/menulaunch.html>`_
  in the desktop menu for selecting software and compute resources and launching jobs on compute nodes using
  `LSF <https://www.ibm.com/support/knowledgecenter/en/SSWRJV_10.1.0/lsf_welcome/lsf_welcome.html>`_.
- `New and updated GUI applications <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/userguide/html/overview.html>`_
  including `Atom <https://atom.io/>`_, `DBeaver <https://dbeaver.io/>`_, `Eclipse <https://www.eclipse.org/>`_,
  `Emacs <https://www.gnu.org/software/emacs/>`_, `gVim <https://www.vim.org/download.php>`_,
  `Octave <https://www.gnu.org/software/octave/index>`_, `QGIS <https://www.qgis.org>`_, `Rstudio <https://rstudio.com/products/rstudio/>`_,
  `Spyder <https://www.spyder-ide.org/>`_, and `VScode <https://code.visualstudio.com/>`_.
-  New and updated command-line utilities, including `CoreUtils <https://www.gnu.org/software/coreutils/>`_,
   `fzf <https://github.com/junegunn/fzf>`_, `fd <https://github.com/sharkdp/fd>`_, `Git <https://git-scm.com/>`_,
   `mycli <https://www.mycli.net/>`_, `rclone <https://www.mycli.net/>`_, `ripgrep <https://github.com/BurntSushi/ripgrep>`_, and more.
- `Conda and Lmod environments <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/userguide/html/commandline.html>`_
  to make it easy to run different versions of popular software.
- `JupyterLab <https://jupyter.org/>`_ with Mathematica, Octave, Python, R, SAS, and Stata kernels (currently disabled pending approval to run Jupyter on the HBS Grid).
- Utilities for monitoring available resources, submitting batch jobs, monitoring running jobs, and customizing the HBS Grid desktop environment.
- Documentation integrated with the gnome desktop.


Existing Installation on the HBS Grid
-------------------------------------

An unofficial `installation of this software is available <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/userguide/html>`_ on the `HBS Grid <https://grid.rcs.hbs.org>`_. These unofficial software installations 
may be more up-do-date, complete, and perhaps more convenient than the
`applications officially supported on the HBS Grid <https://grid.rcs.hbs.org/grid-software>`_.

See the `user guide <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/userguide/html>`_
for instructions if you are an HBS Grid user and wish to try it out.

These installations are **not officially supported** on the HBS Grid and
**any and all use is at your own risk**.


Installation Instructions
--------------------------

NOTE: If you have an account on the HBS Grid your can follow the instructions in the 
`user guide <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/userguide/html>`_
to try it out.

To set up this environment on your own Linux system, either clone 
`the repository <https://code.harvard.edu/HBS/rcs__cluster_software_modules>`_
or `download a released version <https://code.harvard.edu/HBS/rcs__cluster_software_modules/releases>`_.
from the top-level directory run ``make devel GRID_EXP_ROOTDIR=</path/to/installation/directory>`` to 
install a "minimal" system for testing, or ``make all GRID_EXP_ROOTDIR=</path/to/installation/directory>``
to install the full environment (requires about 60 GB of storage space!).

See `here <https://code.harvard.edu/pages/HBS/rcs__cluster_software_modules/devops_docs/html/index.html>`_ for
detailed documentation.

Note that while this system is designed to work with 
`RHEL <https://access.redhat.com/products/red-hat-enterprise-linux>`_ 
(or `Centos <https://www.centos.org/>`_) 7 / `GNOME <https://www.gnome.org/>`_ 3, 
you can install it on just about any Linux system. Some desktop integrations will not 
work without GNOME 3 however. Similarly, this software was designed for systems running 
`LSF <https://www.ibm.com/support/knowledgecenter/SSWRJV_10.1.0/lsf_welcome/lsf_welcome.html>`_, 
and some things will not work correctly on systems where LSF is not available, or even on systems 
where LSF is configured differently than it is on the `HBS Grid <https://grid.rcs.hbs.org>`_. 
It can however still be useful to install on other systems for testing or development purposes.
