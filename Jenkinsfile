@Library('roboshop-shared-library') _

pipeline {
    agent { label 'work-station' }
    stages {
        stage ('Lint Check') {                      // start the stage
            steps {
                script {
                    nodejs.lintChecks()
                }
            }    
        }
        stage('Code Compile') {
            steps {

                     sh "npm install"

            }
        }                                               // end of this stage
    }
}

// @Library('roboshop-shared-library') _ this is shared library we are calling it jenkins shared library For ref go with the shared library repo readme file using this expression we are calling it from the shared library "and itshould alway in the start of the line and it should not be at the end of the line" 
