pipeline {
    agent any

    stages {
	sh "chmod +x gradlew"
	stage('Test') {
            steps {
                echo 'Testing..'
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
