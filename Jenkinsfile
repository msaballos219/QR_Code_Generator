pipeline {
    agent any
    stages {
        stage('SonarQube analysis') {
            steps {
                withSonarQubeEnv('http://10.10.0.48:9000') {
                    sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=QR_Code_Generator -Dsonar.host.url=http://10.10.0.48:9000 -Dsonar.login=11883e7e8136c66e0ad4f054508f141ae3'
                }
            }
        }
    }
}
