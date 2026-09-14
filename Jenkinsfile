pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Node Version') {
    steps {
        sh '''
            export PATH="/var/lib/jenkins/tools/jenkins.plugins.nodejs.tools.NodeJSInstallation/NodeJS-26/bin:$PATH"
            node --version
            npm --version
        '''
    }
}

        stage('Install Dependencies') {
            steps {
                sh 'npm ci'
            }
        }
    }
}