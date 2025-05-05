pipeline {
    agent any

    environment {
        MY_VAR = 'HelloFromEnv'
        PROJECT_NAME = 'JenkinsPipelineDemo'
    }

    stage('Clone Repo') {
    steps {
        echo 'Cloning the repository...'
        git branch: 'main', url: 'https://github.com/Seajal-S/jenkins-pipeline-demo.git'
    }
}


        stage('Run Shell Script') {
            steps {
                echo 'Executing shell script...'
                sh 'chmod +x script.sh && ./script.sh'
            }
        }

        stage('List Working Directory') {
            steps {
                echo 'Listing contents of the workspace...'
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Print Environment Variables') {
            steps {
                echo "Value of MY_VAR is: ${env.MY_VAR}"
                echo "Value of PROJECT_NAME is: ${env.PROJECT_NAME}"
                sh 'echo "Environment variable inside shell: $MY_VAR"'
            }
        }
    }
}
