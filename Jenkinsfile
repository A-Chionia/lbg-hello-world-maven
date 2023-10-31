pipeline {
    agent any
    //ggg
    tools {
        maven "M3"
    }
    stages {
        stage('Checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/A-Chionia/lbg-hello-world-maven.git'
            }
        }
        
        stage('Compile'){
            steps{
                sh "mvn clean compile"
            }
        }
        stage('Test')
        {
            steps{
                sh "mvn test"
            }
        }
        stage('Package'){
            steps{
                sh "mvn package"
                sh "mvn -Dmaven.test.skip -Dmaven.test.skip package"
            }
        }
    }
}