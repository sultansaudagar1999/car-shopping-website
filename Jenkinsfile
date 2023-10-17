pipeline {
    agent any
    stages {
        stage("Code Cloning"){
            steps{
                git url : "https://github.com/sultansaudagar1999/car-shopping-website.git" , branch: "main"
                echo "code cloned succesfully"
            }
        }
        stage("Code Building"){
            steps{
                sh "docker build . -t my-app"
                echo "code build succesfully"
            }
        }
        stage("Code Deploying"){
            steps{
                sh "docker-compose down && docker-compose up -d"
                echo "code deployed succesfully"
            }
        }
    }
}
