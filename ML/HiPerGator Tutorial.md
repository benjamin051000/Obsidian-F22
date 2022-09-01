# Create Account
make a folder in `/blue/eel5934/<gatorlink>`
Submitting jobs: Add class account `--account=eel5934 --qos=eel5934`


# Storage
# ~
- 40GB limit in ~
- do not use for job i/o
- week of snapshots at ~/.snapshot

## Blue Storage
`/blue/eel5934/<user>`
- 2TBlimit per class
- all job i/o should go there
- Make a symlink in ~ to here (for easy access in Jypter nb)

# Jupyter Hub & On-Demand
https://jhub.rc.ufl.edu
https://ood.rc.ufl.edu

In Jupter, choose:
- 1 Core
- 16GB RAM
- --account=eel5934
- --qos=eel5934
	- You can leave account and qos blank IF you're only using this for *this* course.
- Job hours = number of hours you plan to work
- Cluster partition = gpu
- --gres = gpu:a100:1

# NB Kernels
- For generic stuff: Use UFRC Python 3.8
- Tensorflow-2.7.0

**If you get import errors:** ensure you have the right kernel selected!


# Python Packages
- You *can* use `pip`, but be aware that this may cause conflicting issues
- Better solution: Use an environment! `conda`/`mamba`

tip: https://help.rc.ufl.edu has a wiki on how to do various stuff


