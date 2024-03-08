pipeline {
    agent any
    
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment {
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'Ruby@123'
        SNAP_REPO = 'vprofile-snapshot'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '192.168.2.212'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage ('Build') {
            steps {
                sh 'mvn -U clean install'
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
        
    }
}