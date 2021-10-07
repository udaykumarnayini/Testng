 pipeline {
     agent any
     
     environment {
             NEXUS_CREDS = credentials('nexus-private')
             JAVA_HOME = "${JAVA_HOME_ADOPTJDK11}"
     }
     stages {

         stage ('Build') {
                    steps {
                        sh 'chmod +x gradlew'
                        sh './gradlew clean build -Ddataproviderthreadcount=1'
                    }

         }
     }
 }


