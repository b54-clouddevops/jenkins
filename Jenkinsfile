pipeline {
    agent any
    environment {
        ENV_URL         = "pipeline.google.com"                  // Pipeline variable
        SSHCRED         = credentials('SSH_CRED') 
    }
    stages {
        stage('Stage One') {
            steps {    
                    sh '''
                        echo DevOps Training
                        echo AWS Training
                        echo Batch54
                        echo Name of the URL is ${ENV_URL}
                        
                        env 
                    '''
            }
        }

        stage('Stage Two') {
            environment {
                ENV_URL = "stage.google.com"                  // Stage  variable
            }
            steps {                 
                echo "This is stage two"
                echo  "Name of the URL is ${ENV_URL}"
            }
        }

        stage('Stage Three') {
            steps {                 
                echo "This is stage three"
                echo "Name of the URL is ${ENV_URL}"
                sh echo -e "\\e[32m Hai \\e[0m"
            }
        }
    }
}