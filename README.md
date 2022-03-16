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

ci
==
https://jsramblings.com/continuously-deploy-a-react-app-to-gitlab-pages/

stages:
  - build

build:
  image: node:latest    # Run the job in a `node` docker image
  stage: build
  script:
    - yarn install      # Run `yarn install` and `yarn build`
    - yarn build
  artifacts:
    paths:
      - build/          # Save the build result as an artfact









# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
