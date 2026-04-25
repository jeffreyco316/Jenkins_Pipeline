pipeline{
    agent any
    environment {
        DIRECTORY_PATH= 'SIT223'
        TESTING_ENVIRONMENT= '6.1P'
        PRODUCTION_ENVIRONMENT= 'ALPHA'
    } 
    stages{
        stage('Build'){
            steps{
                echo 'Fetch the source code from the directory path specified by the environment variabled'
                echo 'Compile the code and generate any necessary artefacts'           
            }
        }
        stage('Test'){
            steps{
                echo 'Unit tests'
                echo 'Integration tests'
            }
        }
        stage('Code Quality Check'){
            steps{
                echo 'Check the quality of the code'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploy the application to a testing environment specified by the environment variable'
            }
        }
        stage('Approval'){
            steps{
                sleep(time:10,unit:"SECONDS")
            }
        }
        stage('Deploy to Production'){
            steps{
                echo 'Deploying code to the {$PRODUCTION_ENVIRONMENT}'
            }
        }
    }
}
