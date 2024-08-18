pipeline {
    agent any

    stages {
        stage('build image') {
            steps {
                script{
                    sh "go run main.go"
                    //sh "docker run -d  --name jenkines-test jenkines-test"
                }
                
            }
        }
    }
}
