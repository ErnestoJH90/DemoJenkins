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
           sonar.projectKey=demoBB
           #This is the name and version displayed in the SonarQube UI.Was mandatory prior to SonarQube
           sonar.projectName=demoBB
           sonar.projectVersion=1.0

           #Path is relative to the sonar-properties file. Replace "\" by "/" on windows.
           #This property is optional if sonar.modules is set.
           sonar.sources=./

          #Encoding of the source code. Default is Defaultsystem Encoding
          #sonar.sourceEncoding=UTF-8
         }
      }
 
   }
}
