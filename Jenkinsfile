@Library('roboshop-shared-library') _

pipeline {
    agent { label 'work-station' }
    stages {
        stage ('Lint Check') {                      // start the stage
            steps {
                   script {
                        sample.info('USER')     // this is how we call the function in the groovy
                    } 
                    sh "echo installing JSlint"
                    sh "npm i jslint"
                    sh "node_modules/jslint/bin/jslint.js server.js || true"   // this double pipe symbol includes that if the first command is failure make it as a true statement  (that pipe symbol makes forece fully passes the stage)

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
