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
            sh '-S docker images -a'
            sh '''               cd /home/labuser/Downloads/gitrepo/azure-voting-app-redis/azure-vote/azure-vote/
               -S docker images -a
               -S docker build -t jenkins-pipeline .
               -S docker images -a
               cd ..
'''
         }
      }  
      }
    }
