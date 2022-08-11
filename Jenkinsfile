pipeline {
    agent { docker { image 'maven:3.8.4-openjdk-11-slim' } }
    stages {
        stage('deploy') {
            steps {
                retry(3){
                    sh 'mvn --version'
                }
                timeout(time:3, unit: 'MINUTES'){
                    sh 'mvn --version'
                }
            }
        }
    }
}
