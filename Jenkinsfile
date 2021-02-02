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
      stage('Date'){
            steps{
                script{
                    Date date = new Date()
                    env.NAME = date.format("dd-MM-yy")
                }
            }
            post{
                always{
                    script{
                        currentBuild.displayName = "CI/CD-Kt-${NAME}"
                    }
                }
            }
        }
      stage('build') {
            steps {
               sh 'mvn clean package '
         }
       }
   }
}