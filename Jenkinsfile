pipeline{
    agent any
    stages {
        stage('hello'){
            steps{
                sh 'echo hello'
            }
        }
        stage(clean artifact){
            steps{
                sh 'echo hi'
            }
        }
    }
}