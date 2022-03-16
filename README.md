ref
===
https://github.com/gitname/react-gh-pages  

key
===
ssh-keygen -o -t rsa -C "sugoibook@gmail.com"  
ssh-add ~/.ssh/id_rsa  
cat ~/.ssh/id_rsa.pub  
copy to github.com/settings/keys  

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
v17.7.1  

yarn
====
sudo apt-get install curl  
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add  
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list  
sudo apt-get update  
sudo apt-get install yarn  
yarn --version  
1.22.17  

react
=====
npx create-react-app my-app  
cd my-app  
yarn start  

gh-pages
========
npm install gh-pages --save-dev  
nano package.json  
under version, add  
"homepage": "https://sugoibook.github.io/react-deploy",  
nano package.json  
"scripts", before "start", add  
"predeploy": "npm run build",  
"deploy": "gh-pages -d build",  

deploy
======
cd my-app  
npm run deploy  
firefox https://sugoibook.github.io/react-deploy/index.html  
