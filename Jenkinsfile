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
	stage('Package') {
            steps {
                script{
                    pack()
                }
                //sh 'mvn test'
            }
            
        }
        //stage('Deliver') {
            //steps {
                //sh './jenkins/scripts/deliver.sh'
            //}
        //}      
			
        //stage('Checking src') {
            //steps{
                //mySharedLibrary()
            //}
        //}

    }
}
