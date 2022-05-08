pipeline { 
         agent any 
         stages { 
                 stage('One') { 
                 steps { 
                     echo 'Salut, c'est Zulaikha d'edureka' 
                 } 
                 } 
                 stage('Two') { 
                 steps { 
                    input('Voulez-vous continuer ?') 
                 } 
                 } 
                 stage ('Trois') { 
                 when { 
                       not { 
                            branch "master" 
                       } 
                 } 
                 steps { 
                       echo "Bonjour"
                 } 
                 } 
                 stage('Four') { 
                 parallel { 
                            stage('Unit Test') { 
                           steps { 
                                echo "Exécution du test unitaire..." 
                           } 
                           } 
                            stage('Integration test') { 
                              agent { 
                                    docker { 
                                            reuseNode true 
                                            image 'ubuntu ' 
                                           } 
                                    }
                              étapes { 
                                echo "Exécution du test d'intégration..." 
                              } 
                           } 
                           } 
                           } 
              } 
}
