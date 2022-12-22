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
            sh 'sudo docker images -a'
            sh '''               cd /home/labuser/Downloads/gitrepo/azure-voting-app-redis/azure-vote/azure-vote/
               sudo docker images -a
               sudo docker build -t jenkins-pipeline .
               sudo docker images -a
               cd ..
'''
         }
      }  
      }
    }
