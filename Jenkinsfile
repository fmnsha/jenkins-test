pipeline {
    agent any

    stages {
        stage('build image') {
            steps {
                script{
                    sh "docker build -t jenkines-testimage ."
                    //sh "docker run -d  --name jenkines-test jenkines-test"
                }
                
            }
        }
    }
}
