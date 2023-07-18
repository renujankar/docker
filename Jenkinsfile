pipeline {
      agent any 
          stages {
               stage ('stage-1') {
                   steps {
              
                      sh "docker run -itdp 90:80 --name 23Q1 httpd"
                      sh "docker cp /mnt/docker/index.html 23Q1:/usr/local/apache2/htdocs"
                      sh "docker stop 23Q1"
                      sh "docker rm 23Q1" 
                      sh "docker run -itdp 90:80 --name 23Q1 httpd"
                      sh "docker cp /mnt/docker/index.html 23Q1:/usr/local/apache2/htdocs"
                   }
               }
          }
}

