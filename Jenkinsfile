#!/usr/bin/env groovy
pipeline {
agent any
stages {
stage('Build') {
steps {
sh "php -v"
sh "composer -V"
sudo cp -v $WORKSPACE/src/HelloWorld/Greetings.php /var/www/html/
sudo systemctl restart httpd
}
}
stage('Done') {
steps {
echo "Done"
}
}
}
}
