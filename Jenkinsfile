pipeline {
      agent any 
          stages {
               stage ('deploy-23Q2') {
                     steps {
                          sh "docker run -itdp 8080:80 --name 23qq2 httpd"
                          sh "docker cp /mnt/docker/index.html 23qq2:/usr/local/apache2/htdocs" 
                           sh "docker start 23qq2"
                     }
                }
          }
}
