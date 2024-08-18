pipeline {
    agent any

    stages {
        stage('build image') {
            steps {
                sh "docker build -t jenkines-test ."
                sh "docker run -d  --name jenkines-test jenkines-test"
            }
        }
    }
}
