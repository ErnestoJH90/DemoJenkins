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
                        currentBuild.displayName = "node-app-${NAME}"
                    }
                }
            }
        }
      stage('build') {
            steps {
                   Maven(maven:'Maven 3.6.3') {
                  sh 'mvn clean package '
            }
         }
      }
   }
}