# Create Account
make a folder in `/blue/pre1234/<gatorlink>`
Submitting jobs: Add class account `--account=pre1234 --???=pre1234`


# Storage
# ~
- 40GB limit in ~
- do not use for job i/o
- week of snapshots at ~/.snapshot

## Blue Storage
`/blue/pre1234/<user>`
- 2TBlimit per class
- all job i/o should go there

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

