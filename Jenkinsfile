pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('check ip') {
         steps{
            sh 'ip addr show'
         }
      }
      stage('fecha'){
         steps{
            script{
               Date date = new Date()
               env.NAME = date.format("dd-MM-yyyy")
            }
         }
      }
      stage('build') {
            steps {
                    withMaven(maven:'Maven 3.6.3') {
                        sh 'mvn clean package '
            }
         }
      }
   }
}




