
pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                echo "Pulling code from Git repository"
                git 'https://github.com/GeekDaksh/jenkins.git'
            }
        }

        stage('Build') {
            steps {
                echo "Running Build"
                sh 'chmod +x Build.sh'
                sh './Build.sh'
            }
        }

        stage('Test') {
            steps {
                echo "Running Tests"
                sh 'chmod +x Test.sh'
                sh './Test.sh'
            }
        }

        stage('Quality Check') {
            steps {
                echo "Running Quality Checks"
                sh 'chmod +x Quality.sh'
                sh './Quality.sh'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying Application"
                sh 'chmod +x Deploy.sh'
                sh './Deploy.sh'
            }
        }

        stage('Create JOB Directories') {
            steps {
                echo "Creating directory structure"
                sh '''
                mkdir -p JOB_1/JOB_2/JOB_3
                '''
            }
        }

    }
}
