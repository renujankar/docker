pipeline {
      agent any 
          stages {
               stage ('stage-1') {
                     steps {
                         /* sh "yum install docker -y"
                           sh "systemctl start docker"*/
                           sh "systemctl status docker"
                           //sh "systemctl enable docker"//
                     }
                }
                  stage ('stage-2') {
                           steps {
                              sh "docker pull httpd" 
                              sh "docker stop 23Q1"
                              sh "docker rm 23Q1"
                              sh "docker system prune -a -f"
                              sh "docker run -itdv /mnt:/usr/local/apache2/htdocs httpd "
                              sh "docker run -itdp 80:80 --name 23Q1 httpd"
                              sh "docker cp index.html 23Q1:/usr/local/apache2/htdocs"
                              sh "docker exec 23Q1 chmod -R 777 /usr/local/apache2/"
                           }
                  }
                
          }
}

