pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Build Stage automatically'
                sh 'mvn clean install'
                }
        }
         stage('Deploy') {
            steps {
                echo 'Deploy'
                sh 'sudo cp /var/lib/jenkins/.m2/repository/example/demo/helloworld/1.0/helloworld-1.0.war /opt/apache-tomcat-10.1.39/webapps'
                }
         }
         stage('Test') {
            steps {
                echo 'Test'
            }
        }
    }
}
