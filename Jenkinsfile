pipeline {
   agent any
   environment {
       BranchName="master"
   }
   stages {
      stage('Start build') {
         steps {
            echo 'pwd'
            //sleep 360
            sleep 30
            //dir('/var/jenkins_home/workspace') {
               //sh 'ps'
            //}
            echo 'Build runing'
            sh "ps -a"
         }
      }
      stage('Code review'){
         steps {
           echo "This is Codeing......"
           sleep 15
           sh "pwd"
           echo "runing master"
         }
      }
      stage('Test runing'){
         when {
            branch 'master'
         }
         steps {
           //sleep 15
           echo "runing master"
         }
      }
      stage('Deploy ending') {
         environment {Description="This is "}
         steps{
            script{
               if (env.GIT_BRANCH == 'origin/master'){
                  echo "${Description}${BranchName}"
                  //sleep 25
                  sh "ls"
               }
            }
         }
      }
   }
}
