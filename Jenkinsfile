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
               env.NAME = date.format("yyyy-MM-dd")
            }
         }
      }
   }
}




