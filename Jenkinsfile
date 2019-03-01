
pipeline{
    agent any
    tools{
        maven 'maven3.6.0'
        jdk 'java1.8.0'
    }
    stages{
        stage('build'){
            steps{
            sh "mvn -B -DskipTests clean package"
            }
        }
        stage('UnitTest'){
            steps(){
                sh "mvn test"
            }
        }
         stage('Deploy'){
            steps(){
                sh "java -jar target/simple-java-maven-app*.jar"
            }
        }
    }
}
