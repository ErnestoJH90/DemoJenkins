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
      stage('date') {
         script{
            Date date = new Date()
            env.NAME = date.format("dd-mm-yyyy")
         }
      }
   }
}




