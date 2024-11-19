pipeline {
    agent none
    stages {
        stage('Test Job') {
            agent { label 'test-node' }
            steps {
                echo 'Running tests...'
            }
        }
        stage('Prod Job') {
            agent { label 'prod-node' }
            steps {
                echo 'Deploying to production...'
                sh 'scp -i /home/ubuntu/.ssh/id_ed25519 file-to-copy user@10.0.1.40:/home/ubuntu/jenkins'
            }
        }
    }
}
