pipeline {

    agent {
        node {
            label 'master'
        }
    }

    tools { 
        maven 'maven3' 
    }

    options {
        buildDiscarder logRotator( 
                    daysToKeepStr: '15', 
                    numToKeepStr: '10'
            )
    }

    environment {
        APP_NAME = "STUDENT_APP"
        APP_ENV  = "DEV"
    }

    stages {
        
        stage('Stage1_9225101A') {
            steps {
                sh """
                echo "Stage1_9225101A : Release Environment Preparation Completed."
                """
            }
        }

        stage('Stage2_9225101A') {
            steps {
               sh """
                echo "Stage2_9225101A : Release Container WebApp_9225101AAini Created Completed."
                """
            }
        }

        stage('S3_9225101A'){
            parallel {
                stage('S3_API TEST') {
                    steps {
                        sh """
                        env 
                        """
                    }
                }

                stage ('S3 SCAN TEST') {
                    steps {
                        shh 'echo "Hello Student. Thanks for keeping up!"'
                    }
                }
                

        stage('Printing All Global Variables') {
            steps {
                sh """
                env
                """
            }
        }

    }   
}
    }
}
