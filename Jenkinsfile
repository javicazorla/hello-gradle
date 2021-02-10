pipeline {

    agent any

    stages {
        stage('Publish artifacts'){
            steps {
                withCredentials([
                    string(credentialsId: 'gitLabPrivateToken', 
                    variable: 'TOKEN')
                    ]){
                        sh './gradlew publish'
                    }
            }
        }
    }
}
