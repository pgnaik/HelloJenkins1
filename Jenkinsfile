pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/pgnaik/HelloJenkins1.git']])
            }
        }
        
        stage('Build') {
            steps {
                git 'https://github.com/pgnaik/HelloJenkins1.git'
                bat '''javac HelloJenkins.java
                       java HelloJenkins'''
            }
        }
        
        stage('Test') {
            steps {
                echo "Java program is executing successfully...."
            }
        }


    }
}
