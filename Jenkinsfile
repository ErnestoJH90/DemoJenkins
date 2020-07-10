pipeline {
   agent any

   stages {
     stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Test') {
         steps {
            echo 'How are you World'
            stage('SonarQube') {
         steps {
           echo 'scanner'
             }
           }
         }
      }
      stage('Deploy') {
         steps {
            echo 'GoodBye World'
         }
      }
       stage('PowerShell') {
         steps {
            powershell label: '', script: 'Write-Output "Hello PowerShell!"'
         }
      }
   }
}
