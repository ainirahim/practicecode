pipeline {

    agent any
stages {
        
        stage('Stage1_9225101A') {
            steps {
                echo "Stage1_9225101A : Release Environment Preparation Completed."
            
            }
        }

        stage('Stage2_9225101A') {
            steps {
                echo "Stage2_9225101A : Release Container WebApp_9225101AAini Created Completed."
        
            }
        }

        stage('S3_9225101A'){
            parallel {
                stage('S3_API TEST') {
                    steps {
                       echo 'Stage3_9225101A: API Test Completed'
                    }
                }

                stage ('S3 SCAN TEST') {
                    steps {
                        echo 'Stage3_9225101A: Scan Test Completed'
                    }
                }
            }
        }

                 stage ('S4_9225101A') {
                    input {
                        message "9225101A, proceed to release the work to next phase?"
                        ok "Stage5_9225101A : Work Release - Proceed to Next Phase"
                    }
                     steps {
                         echo 'S5_9225101A'
                     }
                }

                stage ('S5_9225101A') {
                steps {
                    echo 'Stage5_9225101A : Work Release -Stops'
                }
                }
                

    }   
}
    

