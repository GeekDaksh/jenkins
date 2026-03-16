pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'chmod +x Build.sh'
                sh './Build.sh'
            }
        }

        stage('Test') {
            steps {
                sh 'chmod +x Test.sh'
                sh './Test.sh'
            }
        }

        stage('Deploy') {
            steps {
                sh 'chmod +x Deploy.sh'
                sh './Deploy.sh'
            }
        }

        stage('Create JOB Directories') {
            steps {
                sh 'mkdir -p JOB_1/JOB_2/JOB_3'
            }
        }

    }
}
