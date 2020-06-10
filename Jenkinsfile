pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout'
            }
        }
        stage('Build') {
            steps {
                echo ''
                sh 'mvn clean package'
            }
        }
        //stage('Test') {
          //  steps {
            //    echo 'Testing'
              //  bat 'mvn test'
            //}
        //}
       // stage('JaCoCo') {
         //   steps {
           //     echo 'Code Coverage'
             //   jacoco()
            //}
        //}
        stage('Sonar') {
            steps {
                echo 'Sonar Scanner'
               	def scannerHome = tool 'SonarQube Scanner 3.0'
			    
			    }
            }
        }
        //stage('Package') {
           // steps {
             //   echo 'Packaging'
               // bat 'mvn package -DskipTests'
            //}
        //}
        stage('Deploy') {
            steps {
                echo '## TODO DEPLOYMENT ##'
            }
        }
    }
    
    post {
        always {
            echo 'JENKINS PIPELINE'
        }
        success {
            echo 'JENKINS PIPELINE SUCCESSFUL'
        }
        failure {
            echo 'JENKINS PIPELINE FAILED'
        }
        unstable {
            echo 'JENKINS PIPELINE WAS MARKED AS UNSTABLE'
        }
        changed {
            echo 'JENKINS PIPELINE STATUS HAS CHANGED SINCE LAST EXECUTION'
        }
    }
}
