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


