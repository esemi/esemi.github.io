
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt-get update
sudo apt install -y git mousepad gnome-software software-properties-common curl
sudo apt install -y python3.12 python3.12-dev python3.12-venv
sudo apt install -y redis mysql sbt default-jre unzip
curl -sS https://bootstrap.pypa.io/get-pip.py | python3.10
curl -sS https://bootstrap.pypa.io/get-pip.py | python3.12

echo "deb https://repo.scala-sbt.org/scalasbt/debian all main" | sudo tee /etc/apt/sources.list.d/sbt.list
echo "deb https://repo.scala-sbt.org/scalasbt/debian /" | sudo tee /etc/apt/sources.list.d/sbt_old.list
curl -sL "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x2EE0EA64E40A89B84B2DF73499E82A75642AC823" | sudo apt-key add
sudo apt-get update


echo "alias gitpurge='git branch | grep -v master | grep -v grap | xargs -n 1 git branch -D'" >> ~/.bashrc
echo "export USE_GKE_GCLOUD_AUTH_PLUGIN=True" >> ~/.bashrc
echo "export PATH=~/.kubectx:$PATH" >> ~/.bashrc
echo "export PATH=~/.kubens:$PATH" >> ~/.bashrc

install chrome-stable
install lastpass

login esemiko@gmail.com + lastpass

install telegram

login s.efremov@semrush.com + lastpass
install slack

setup rus keyboard layout
setup marblemouse

mkdir -p ~/development
cd  ~/development
chmod 700 ~/.ssh
chmod 600 ~/.ssh/id_rsa
chmod 644 ~/.ssh/*.pub

git checkout official-documents from github
git checkout invest_stat from github
git checkout epsa-farm from github + .env
git checkout esemi.github.io


install pycharm-community
import settings

install idea-community
sudo apt-get install sbt default-jre

mkdir -p ~/repos
cd ~/repos
git checkout corporate-ui from gitlab + .env
git checkout corporate-admin from gitlab + .env
git checkout corporate-api from gitlab + .env
git checkout cobalt-clients from gitlab + .env
git checkout sharing-ui from gitlab + .env
git checkout sharing-grpc from gitlab + .env

console.google.com

cp backup/.kube ~/.kube


sudo apt-get install apt-transport-https ca-certificates gnupg curl
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
sudo apt-get install google-cloud-sdk-gke-gcloud-auth-plugin

kubectl
kubectx
kubens


sudo apt-get install gnupg curl
curl -fsSL https://www.mongodb.org/static/pgp/server-7.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \
   --dearmor
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list

sudo apt-get update
sudo apt-get install -y mongodb-org
sudo apt-get install -y default-libmysqlclient-dev pkg-config gcc gettext-base

