pipeline {

          agent any
          environment {       
             PYTHON_HOME =  '/usr/bin/python3'         
         }
            
          stages {

              stage('Build') {

                  steps {

                      script {

                          // Choisissez la commande en fonction de votre script
                          sh 'pip install -r requirements.txt'
                          sh 'python3 scraper.py'
                          archiveArtifacts artifacts: 'data.csv', fingerprint: true
                      }

                  }

              }
           
         }
  }
