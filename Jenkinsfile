pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/BharatKumarG/FullStack-Assignment-1.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Use absolute path if necessary
                sh '/usr/bin/npm install'
            }
        }

        stage('Run Tests') {
            steps {
                // Use absolute path if necessary
                sh '/usr/bin/npm test'
            }
        }

        stage('Build') {
            steps {
                // Use absolute path if necessary
                sh '/usr/bin/npm run build'
            }
        }

        stage('Deploy') {
            steps {
                sh 'scp -r ./dist user@server:/path/to/deploy'
            }
        }
    }
}
