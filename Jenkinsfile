pipeline {
    agent any
    
    stages {
        stage('BuildApp') {
            steps {
                echo 'Build Stage automatically'
                sh 'mvn clean install'
                }
        }
         stage('DeployApp') {
            steps {
                echo 'Deploy'
                sh 'sudo cp /var/lib/jenkins/.m2/repository/example/demo/helloworld/1.0/helloworld-1.0.war /root/apache-tomcat-11.0.0-M21/webapps'
                }
         }
         stage('TestApp') {
            steps {
                echo 'Test Application'
            }
        }
    }
}
