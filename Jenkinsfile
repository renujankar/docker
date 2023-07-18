pipeline {
      agent any 
          stages {
               stage ('deploy-23Q2') {
                     steps {
                          sh "docker run -itdp 8081:80 --name 2023Q2 httpd"
                          sh "docker cp /mnt/docker/index.html 2023Q2:/usr/local/apache2/htdocs" 
                     }
                }
          }
}
