pipeline {
 agent any
 tools {
  maven 'maven3.6.0'
  jdk 'java1.8.0'
 }
 stages {
  stage('build') {
   steps {
    sh "mvn -B -DskipTests clean package"
   }
  }
  /*stage('UnitTest') {
   steps {
    sh "mvn test"
   }
   post {
    always {
     junit 'target/surefire-reports/*.xml'
    }
   }
  }*/
  stage('Deploy') {
   steps {
    sh "java -jar target/my-app-1.0-SNAPSHOT.jar"
   }
  }
  /*stage('publish') {
   steps {
    sh 'curl -X PUT -u admin:APB4oSbMxjG67dX7gZdt2oPHD4m -T target/my-app-1.0-SNAPSHOT.jar "http://34.220.183.178:8081/artifactory/libs-snapshot/my-app-1.0-SNAPSHOT.jar"'
   }
  }*/
 }
}
