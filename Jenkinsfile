pipeline {
   agent {
    label:"docker"
   }
   stages{
    stage('Build Go Application') {
            steps {
                sh 'go build -o main'
            }
        }
       stage('Create Docker Image') {
            steps {
                sh 'docker build -t myapp:latest .'
            }
        }
       
   }

}