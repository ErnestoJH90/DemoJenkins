pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('SonarQube') {
         steps {
           #must be unique in a given SonarQube instance
            sonar.projectKey=demojenkins
            #This is the name and version displayed in the SonarQube UI.Was mandatory prior to SonarQube
            sonar.projectName=demojenkins
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
