pipeline {
    agent { label 'linux-node' }

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t node_$BUILD_NUMBER .'
                sh 'docker run -d -p 3000:3000 node_$BUILD_NUMBER'
              
            }
        }
    }
}
