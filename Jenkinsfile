pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'php -v'
                sh 'composer -V'
                sh 'composer install'
                sh 'cp -v $WORKSPACE/src/HelloWorld/Greetings.php /var/www/html/'
                sh 'systemctl restart httpd'
            }
        }
    }
}
