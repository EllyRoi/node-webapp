pipeline {
    agent { label 'linux-node' }

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t node_$BUILD_NUMBER -f /home/rfrancisco/node-webapp .'
                sh 'docker run -p 3000:3000 node_$BUILD_NUMBER'
              
            }
        }
    }
}
