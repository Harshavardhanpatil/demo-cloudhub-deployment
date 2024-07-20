pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -U -e -v clean -DskipTests package'
            }
        }

        stage('Deployment') {
            steps {
                bat 'mvn -U -V -e -B package deploy -DmuleDeploy'
            }
        }
    }
}
