pipeline {
    agent any
    
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment {
        NEXUS_USER = 'admin'
        NEXUS-PASS = 'Ruby@123'
        SNAP_REPO = 'vprofile-snap'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vprofile-maven-central'
        NEXUSIP = '192.168.2.212'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage ('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
        
    }
}