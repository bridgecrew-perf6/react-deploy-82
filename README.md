key
===
ssh-keygen -o -t rsa -C "sugoibook@gmail.com"
ssh-add ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub
# copy to github.com/settings/keys

git
===
git config --global user.name "you"
git config --global user.email "you@example.com"
git config -l

node
====
sudo apt-get update
sudo apt-get install npm
sudo npm install -g n
sudo n stable
sudo n latest
node --version
# v17.7.1

react
=====
npx create-react-app my-app
