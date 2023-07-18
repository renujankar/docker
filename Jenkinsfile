pipeline {
      agent any 
          stages {
               stage "stahge-1" {
                   steps {
                      sh "docker -itdp 90:80 --name 23Q1 httpd"
                      sh "docker cp /mnt/docker/index.html 23Q1:/usr/local/apache2/htdocs"
                   }
               }
          }
}

