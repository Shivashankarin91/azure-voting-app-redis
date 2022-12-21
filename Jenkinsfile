pipeline{
    agent any
        stages{
            stage('Veified Branch'){
                steps{
                echo "$GIT_BRANCH"                    
                }
            }
      stage('Docker Build') {
         steps {
            sh 'docker images -a'
            sh '''               cd /home/labuser/Downloads/gitrepo/azure-voting-app-redis/azure-vote/azure-vote/
               docker images -a
               docker build -t jenkins-pipeline .
               docker images -a
               cd ..
'''
         }
      }  
      }
    }
