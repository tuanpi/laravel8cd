pipeline {
    agent any
    environment {
                DB_HOST = credentials("laravel-host1")
                DB_DATABASE = credentials("laravel-database1")
                DB_USERNAME = credentials("laravel-user1")
                DB_PASSWORD = credentials("laravel-password1")
            }
    stages {
        stage("Build") {
            steps {
                sh 'php --version'
                //sh 'composer install'
                sh 'composer --version'
                sh 'cp .env.example .env'
                sh 'echo $DB_HOST'
                sh 'echo $DB_USERNAME'
                sh 'echo $DB_DATABASE'
                sh 'echo $DB_PASSWORD'
                
                
                //sh 'echo DB_HOST=${env.DB_HOST} >> .env'
                //sh 'echo DB_USERNAME=${env.DB_USERNAME} >> .env'
                //sh 'echo DB_DATABASE=${env.DB_DATABASE} >> .env'
                //sh 'echo DB_PASSWORD=${env.DB_PASSWORD} >> .env'
                //sh 'php artisan key:generate'
                //sh 'cp .env .env.testing'
                //sh 'php artisan migrate'
            }
        }
        stage("Unit test") {
            steps {
                //sh 'php artisan test'
                echo "Unit test"
            }
        }
        stage("Code coverage") {
            steps {
                //sh "vendor/bin/phpunit --coverage-html 'reports/coverage'"
                echo "Code coverage"
            }
        }
        stage("Static code analysis larastan") {
            steps {
                //sh "vendor/bin/phpstan analyse --memory-limit=2G"
                echo "Code coverage"
            }
        }
        stage("Static code analysis phpcs") {
            steps {
                //sh "vendor/bin/phpcs"
                echo "Code coverage"
            }
        }
        stage("Docker build") {
            steps {
                //sh "docker build -t danielgara/laravel8cd ."
                echo "Code coverage"
            }
        }
        //stage("Docker push") {
            //environment {
            //    DOCKER_USERNAME = credentials("docker-user")
            //    DOCKER_PASSWORD = credentials("docker-password")
            //}
            //steps {
            //    sh "docker login --username ${DOCKER_USERNAME} --password ${DOCKER_PASSWORD}"
            //    sh "docker push danielgara/laravel8cd"
            //}
            //echo "Code coverage"
        //}
        stage("Deploy to staging") {
            steps {
                //sh "docker run -d --rm -p 80:80 --name laravel8cd danielgara/laravel8cd"
                echo "Code coverage"
            }
        }
        stage("Acceptance test curl") {
            steps {
                //sleep 20
                //sh "chmod +x acceptance_test.sh && ./acceptance_test.sh"
                echo "Code coverage"
            }
        }
        //stage("Acceptance test codeception") {
        //    steps {
        //        sh "vendor/bin/codecept run"
        //    }
         //   post {
        //        always {
        //            sh "docker stop laravel8cd"
        //        }
        //    }
        //}
    }
}
