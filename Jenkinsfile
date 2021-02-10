pipeline {

    agent any

    stages {
        stage('Publish artifacts'){
            steps {
                withCredentials([string(credentialsId: 'gitLabPrivateToken', variable: 'token')]) {
                    withGradlew {
                        sh './gradlew publish'
                    }
                }
            }
        }
    }
}
