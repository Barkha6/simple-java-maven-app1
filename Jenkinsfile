pipeline {
    agent any
    stages {
	    stage('Git Check Out') {
            steps {
           	gitCheckOut(
                    branch: "main",
                    url: "https://github.com/Barkha6/simple-java-maven-app.git"
                )
            }
        }
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
	}		
            //post {
                //always {
                    //junit 'target/surefire-reports/*.xml'
                //}
            //}
        //}
      stage('Package'){
          steps{
              sh "mvn package"
        }
      }
      stage('Sonar Scan'){
          steps{
            withSonarQubeEnv('sonar') {
            sh "mvn sonar:sonar"
          }
        }
      }	
        //stage('Deliver') {
            //steps {
                //sh './jenkins/scripts/deliver.sh'
            //}
        //}
    }
}
