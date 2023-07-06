pipeline {
    agent any
    tools {
        maven "MAVEN3"
        JDK "OracleJDK8"
    }

    environment {
        SNAPSHOTS_REPO = "vprofile-snapshots"
        NEXUS_USER = "admin"
        NEXUS_PASSWORD = "12Adetola"
        CENTRAL_REPO = "vpro-maven-central"
        NEXUS_VERSION = "nexus3"
        NEXUS_PROTOCOL = "http"
        NEXUSIP = '172.31.83.167'
        NEXUS_PORT = "8081"
        NEXUS_REPOSITORY = "vprofile-release"
	    NEXUS_GRP_REPO = "vpro-maven-group"
        NEXUS_CREDENTIAL_ID = "nexuslogin"
        ARTVERSION = "${env.BUILD_ID}"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }   
    }
}