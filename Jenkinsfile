pipeline {
   agent any
   tools{
 maven 'maven'  
   }
    trigger {
  pollSCM '* * * * *'
} 

    stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
         stage('test ') {
            steps {
                sh 'mvn test'
            
            }
         }
          
         stage('deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
}