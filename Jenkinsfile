pipeline {
      agent any 
          stages {
               stage ('deploy-23Q2') {
                     steps {
                          sh "docker run -itdp 8080:80 --name 23q2 httpd"
                          sh "docker cp /mnt/docker/index.html 23q2:/usr/local/apache2/htdocs" 
                     }
                }
          }
}
