pipeline {
    agent {
        label 'my-agent'
    }
    
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
                sh 'sudo cp /var/lib/jenkins/.m2/repository/example/demo/helloworld/1.0/helloworld-1.0.war /opt/apache-tomcat-10.1.39/webapps/'
                }
         }
         stage('TestApp') {
            steps {
                echo 'Test Application'
            }
        }
    }
}
