pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -U -e -v -X clean -DskipTests package'
            }
        }

        stage('Deployment') {
            steps {
                bat 'mvn -U -V -e -B -X package deploy -DmuleDeploy'
            }
        }
    }
}
