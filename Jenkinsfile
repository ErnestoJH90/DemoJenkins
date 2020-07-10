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
      stage('SonarQube') {
         steps {
           echo "$sonar_scanner"
           sonar.projectKey=demojenkins
           sonar.projectName=demojenkins
           sonar.projectVersion=1.0
           sonar.sources=./
         }
      } 
   }
}
