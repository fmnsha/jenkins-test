pipeline {
   agent any



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