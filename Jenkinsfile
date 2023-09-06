pipeline{
    agent any 
    tools{
         maven 'M2_HOME'
    }
    stages{
    stage('maven clean'){
        steps{
        sh  'mvn clean'
        }
    }
    stage('maven install'){
        steps{
          sh  'mvn install'
            
        }
    }
    stage('maven package'){
        steps{
         sh   'mvn package'
        }
    }
    stage('upload artifact'){
        steps{
            sh 'curl --upload-file webapp/target/webapp.war -u admin:devops -v http://ec2-52-91-118-64.compute-1.amazonaws.com:8081/repository/war-files-utc/'
        }
    }


    }

}