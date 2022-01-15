pipeline {
    agent any

    stages {
	stage('Test') {
            steps {
                echo 'Testing..'
	sh "chmod +x gradlew"
	sh " ./gradlew test"
            }
        }

        stage('Build') {
            steps {
                echo 'Building..'
    sh "./gradlew clean build --no-daemon"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
