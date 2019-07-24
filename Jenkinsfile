pipeline {
    agent any

    /*parameters {
         string(name: 'tomcat_dev', defaultValue: '35.166.210.154', description: 'Staging Server')
         string(name: 'tomcat_prod', defaultValue: '34.209.233.6', description: 'Production Server')
    }*/

    /*triggers {
         pollSCM('* * * * *')
     }*/

stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
                sh 'echo $PATH'
                sh "docker build ."/*-t tomcatwebapp:${env.BUILD_ID}*/
            }
           
        }
    }
}