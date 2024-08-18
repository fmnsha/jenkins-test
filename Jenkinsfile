pipeline {
   agent any


   tools {
      go 'golang'
   }
   environment {
       DOCKERHUB_CREDENTIALS = credentials('dockerhub')
       DOCKER_IMAGE = 'ephraimaudu/test-app'
       GITHUB_CREDENTIALS = 'git-secret'
       SONAR_TOKEN = credentials('SONAR_TOKEN')
   }


   stages{
       stage('Checkout'){
           steps{
               echo "checking out repo"
               git url: 'https://github.com/fmnsha/jenkins-test', branch: 'main'
           }
       }
       
       stage('Run Docker Build'){
           steps{
               script{
                    echo "starting docker build"
                    sh "docker build  -t myjenkinstestcon ."
                    echo "docker built successfully"
               }
           }
       }
   }


   post {
       always{
           cleanWs()
       }
   }
}