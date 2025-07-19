# django-todo
A simple todo app built with django

![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)
### Setup
To get this repository, run the following command inside your git enabled terminal
```bash
$ git clone https://github.com/shreys7/django-todo.git
```
You will need django to be installed in you computer to run this app. Head over to https://www.djangoproject.com/download/ for the download guide

Once you have downloaded django, go to the cloned repo directory and run the following command

```bash
$ python manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
$ python manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user
```bash
$ python manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
$ python manage.py runserver
```

Once the server is hosted, head over to http://127.0.0.1:8000/todos for the App.

Cheers and Happy Coding :)

git setup

virtualenv -p python env

source env/bin/activate

cd django-todoapp

pip install django

pip freeze > requirements.txt

git checkout -b feature/deploy-app

git add .git commit -m "message"

curl ifconfig.me          // Ip address of Try accessing your app from EC2 itself

nohup python3 manage.py runserver 0.0.0.0:8002 &    run in deatched mode

 lsof -i:8001    list the services where all run on given port

 kill -9 process id 


 go to ssh ec2 instance 
 create sudo docker pull jenkins/jenkins
 sudo docker run -d -p 80:8080 jenkins:latest

 
cd /home/ubuntu/projects/django-todo
docker build . -t todo-dev
docker run -d -p 8002:8002 todo-dev
check repo         git remote -v
git remote set-url origin our url
check git status
git add .
jenkines run on port 8080

git client  plugin 
configure system
scroll down github
add github server
add credentials
secreate text is personal access token scope(global)   id jenkins-github-cicd
add 
it will show you your git account
create CICD pipeline
source code
gie repo url
give branch name  from github
build step 
execute shell
sudo docker build . -t todo-app
sudo docker run -p 8000:8000 -d todo-app
lsof -i:8000
make master server on ec2 
action -> image and templeates -> launch more like this  make instances 3
open master terminal 
sudo apt get update
sudo apt install ansible
cd .ssh 
vim ansiblekey
paste key
sudo ssh -i ~/.ssh/ansiblekey ubuntu@Ip of instance server3
cat /etc/ansible/hosts
mkdir ansible
cd ansible/
vim hosts
[servers]
server1 ansible_host=ip of server1
server2 ansible_host=ip of server2
server3 ansible_host=ip of server3
[all:vars]
ansible_python_interpreter=/usr/bin/python3
ansible pwd
ansible-inventory --list -y path -i host path is 
cd ..
cd .ssh 
chmod 700 ~/.ssh
chmod 600 ~/.ssh/ansible_key
ansible all -m ping -i inventory_path --private-key=~/.ssh/ansible_key

ansible all -a 'free -h' -i inventory_path --private-key=~/.ssh/ansible_key
# servers from inventory_path this inventory  using --private-key=~/.ssh/ansible_key this private key  show disk space
mkdir playblooks
cd playbooks
vim createbook.yml
---
name: creating the file
hosts: all
become: true
tasks:
  - name: creating file
    File:
    path: /home/ubuntu/myfiles.txt
    state:touch
ansible-playbook createbook.yml -i inventory_path --private-key=~/.ssh/ansible_key
sudo usermod -aG docker $USER && newgrp docker
minikube start --driver=docker
sudo snap install kubectl --classic





