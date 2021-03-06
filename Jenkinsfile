pipeline {
    agent any
    stages {
        stage('Build and deploy') {
            steps {
               
               sh 'faas-cli build -f ./hello-python.yml'
               sh 'faas-cli deploy -f ./hello-python.yml'
               input message: 'Click "proceed" to finish the job'
            }

        }
        stage('Stop process') {
            steps {
                sh 'echo "process stopped"'
            }
        }

    }
}
