@Library('shared-library-barkha') _

pipeline {
    agent {
        label 'java-build-node'
    }
    stages {
        stage('Build') {
            steps {
                script{
                    build()
                }
                //sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                script{
                    test()
                }
                //sh 'mvn test'
            }
            
        }
	stage('Package'){
          steps{
	     script{	   
                 package()
          }
         }   
       }		
        
        //stage('Checking src') {
            //steps{
                //mySharedLibrary()
            //}
        //}

    }
}
