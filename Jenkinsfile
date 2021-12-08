pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh """
                  php -v
                  composer -V
                  composer install
                  sudo cp -v $WORKSPACE/src/HelloWorld/Greetings.php /var/www/html/
                  sudo systemctl restart httpd
                """
            }
        }
    }
