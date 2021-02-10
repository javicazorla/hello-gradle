pipeline {

    agent any

    stages {
        stage('Publish artifacts'){
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'e4ece5bb-ab9d-4194-83af-47d800737040', 
                        passwordVariable: 'PASS', 
			usernameVariable: 'NAME')]
                ){
                    sh './gradlew publish'
                }
            }
        }
    }
}
