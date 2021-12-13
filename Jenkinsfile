#!/usr/bin/env groovy
pipeline {
agent any
stages {
stage('Build') {
steps {
sh "php -v"
sh "composer -V"
sh "sudo cp -v $WORKSPACE/src/HelloWorld/Greetings.php /var/www/html/"
sh "sudo systemctl restart httpd"
}
}
stage('Done') {
steps {
echo "Done"
}
}
}
}
