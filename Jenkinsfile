pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/bhawana59/jenkins-demo-pipeline.git'
            }
        }

        stage('Install Dependencies') {
    steps {
        sh 'python3 -m pip install -r requirements.txt'
    }
}

        stage('Run Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build Completed') {
            steps {
                echo 'Application Build Successful'
            }
        }
    }
}