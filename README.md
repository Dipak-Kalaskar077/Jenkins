# Jenkins Installation Script

sudo apt-get update

sudo apt update

sudo apt install fontconfig openjdk-17-jre -y

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install jenkins -y

cat /var/lib/jenkins/secrets/initialAdminPassword


# Required Plugins for jenkins

1) Git
2) Pipeline Stage view
3) Sonarqube Scanner
4) Sonarqube Quality gate
