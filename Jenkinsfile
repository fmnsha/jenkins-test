pipeline {
    agent any

    stages {
        stage('build image') {
           script{
                    echo "starting docker build"
                    sh "docker build build -t golang-test ."
                    echo "docker built successfully"
               }
           }
        }
    }
}
