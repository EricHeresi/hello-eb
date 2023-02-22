pipeline {
    agent any
    
    options{
        timestamps()
    }
    stages {
        stage('EB create'){
            steps {
                 withAWS(credentials: 'aws-access-key', region: 'eu-west-1') {
                    dir("eb") {
                        sh 'eb create dev-env'
                    }
                 }
            }
        }
    }
}