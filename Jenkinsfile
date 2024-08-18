pipeline {
    agent any

    stages {
        stage('build image') {
            steps {
                docker build -t jenkines-test .
                docker run -d  --name jenkines-test jenkines-test
            }
        }
    }
}
