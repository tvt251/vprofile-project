pipeline {
    agent any
    
    tools {
        maven "MAVEN3"
        jdk "Oracle8JDK"
    }

    environment {

    }

    stages {
        stage ('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
        
    }
}