pipeline {
    agent any
    
    tools {
        maven "jenkin-maven"
    }
    
    stages {
        stage('SCM') {
            steps {
             git 'https://github.com/ashwin1-dev/18-feb-mvn2.git'
                }
            }
            
        stage('BUILD') {
            steps {
                sh "mvn clean package"
                 }
            }
            
        stage('Deploy') {
            steps {
           sh "scp /var/lib/jenkins/workspace/mvn1/target/aaa.war  root@192.168.0.32:/opt/apache-tomcat/webapps/ddd.war"      
                  }
              }
        }
    
}
