
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
#### Creates a custom Jupyter Notebook kernel named "student" for running Python code with specific configurations.
```
python -m ipykernel install --user --name=student
```
#### Go to Git-hub and create a empty public or private repository for project after creating repo their is some commands to initialize the repo on instance the commands is below 
```
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin <your repo url>
git push -u origin main
```
### After that create a 2 file and the file content on my student performance repository
```
touch setup.py requirements.txt
```
#### After adding a file content install the pip file 
```
pip install -r requirements.txt
```
### Create a src folder and in src create ___init__.py file
```
mkdir src
cd src
touch __init__.py
```
### Inside src folder create 2 folder 1st is components and 2nd is pipeline folder  
```
mkdir components pipeline
```
### Inside the components folder create some files 
```
cd components 

touch __init__.py data_ingestion.py data_transformation.py model_trainer.py
```
### Create a file on pipeline folder
```
cd ..
cd pipeline 
touch train_pipeline.py predict_pipeline.py __init__.py

```
### Create file on src folder 
```
cd ..
touch logger.py exception.py utils.py  
cd ..
```
## Run the Logger fil
### The logger file for used to record and track project progress, errors, and decisions for debugging, reproducibility, and documentation purposes.
```
python3 src/logger.py
```
###  After that push all data on git repository
```
git status
git add . 
git commit -m "Logging and exception"
git push -u origin main
```
### Create a notebook folder and inside the create data folder 
### paste the the ipynb file and also the data csv file 
```
mkdir notebook
cd notebook
mkdir data 
cd data 
nano stud.csv
```
## Run the 2 ipynd file on notebook 
### notebook installation commands given below 
```
pip install notebook
```
```
jupyter notebook --generate-config
```
```
jupyter notebook password
```
### nohup command is use for background proccess
```
nohup jupyter notebook ip=0.0.0.0 &
```
### Run the data_ingestion file is used to collect, clean, and prepare data from multiple sources for analysis or machine learning projects.
```
python3 src/components/data_ingestion.py
```
### push the code in git repository
```
git add .
git status 
git commit -m "Model Trainer"
git push -u origin main
```
### Create a application file 
```
nano application.py
```
### Create a templates folder inside the folder create index.heml and home.html file 
```
mkdir templates
cd templates
touch index.html home.html
cd ..
```
### Run the application file to check the application is running or not 
```
python3 application.py
```
### If the successfully application work push the data to git repo
```
git add .
git commit -m "Prediction Pipeline"
git push -u origin main
```
# Deploying Part remaining 
# To be continue .....