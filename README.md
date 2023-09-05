
# Student Performance

A brief description of what this project does and who it's for


### Create a EC2 Instance 

```bash
  Launch Instance
  Name = Student Performance
  AMI = Ubuntu 20.04
  Instance Type = t2.medium 
  Key pair = Existing Key
  Network setting = defualt
  Security Group = All traffic
  Storage = 29 GB

  Launch Instance
```

### After Launch Instance Connect using Putty

```
sudo apt update && sudo apt upgrade -y
```

### Download and Install Maniconda for the Envornment

```
wget https://repo.anaconda.com/miniconda/Miniconda3-py38_23.3.1-0-Linux-x86_64.sh
```
```
bash Miniconda3-py38_23.3.1-0-Linux-x86_64.sh
```
### Activate the conda Envornment
```
source ~/.bashrc
```
### Create a new Envornment for Student Performance
```
conda create -n student python=3.9 ipykernel
```
### And activate the student Envornment
```
conda activate student
```



  
