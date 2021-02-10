pipeline {

    agent any

    stages {
        stage('Publish artifacts'){
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'da142980-f458-481f-b5d5-1ea8f32e3b53', 
                        passwordVariable: 'PASS', 
			            usernameVariable: 'NAME')]
                ){
                    sh './gradlew publish'
                }
            }
        }
    }
}
