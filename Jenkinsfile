pipeline {
      agent any 
          stages {
               stage ('stage-1') {
                   steps {
                      sh "docker run -itdp 90:80 --name 23Q1-1 httpd"
                      sh "docker cp /mnt/docker/index.html 23Q1-1:/usr/local/apache2/htdocs"
                   }
               }

                stage ('stage-2') {
                     steps {
                          sh "docker run -itdp 8080:80 --name 23Q2 httpd"
                      sh "docker cp /mnt/docker/index.html 23Q2:/usr/local/apache2/htdocs" 
                     }
                }
          }
}

