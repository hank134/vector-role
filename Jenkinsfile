pipeline {
    agent {
        label 'linux'
    }
    stages {
        stage('git') {
            steps {
                git branch: 'main', credentialsId: 'c0a5144e-8dab-4c08-b3e9-fd470e090cfc', url: 'git@github.com:hank134/vector-role.git'
                
            }
        }
        stage('moleculeT') {
            steps {
                sh "molecule test"
            }
            
        }
    }
}
