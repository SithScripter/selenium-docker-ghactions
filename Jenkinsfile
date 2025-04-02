pipeline{

    agent any

    stages{

        stage('Build Jar'){
            steps(){
                bat "mvn clean package -DskipTests"
            }

        }

        stage('Build Image'){
            steps(){
                bat "docker build -t=gaumji19/selenium ."
            }

        }

        stage('push image'){
            steps(){
                bat "docker push gaumji19/selenium"
            }

        }

    }

}