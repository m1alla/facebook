
pipeline{

      agent any

parameters {
            string(name: 'Version',
            defaultValue: 'facebook-2.0',
            description: 'facebook project')
           }

     stages
                          stage('Checkout'){
                            steps{
                                      {


                                              checkout([$class: 'GitSCM', branches: [[name: '*/facebook-2.0']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/m1alla/facebook.git']]])


                                      }
                                    }
                             stage('Build'){
                               steps{
                                 script{
sh ' /etc/maven/apache-maven-3.8.4/bin/mvn -f /var/lib/jenkins/workspace/maven-pipeline/pom.xml install'
                                 }
                               }
                             }
                    }



}
