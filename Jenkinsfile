pipeline {
      agent any 
          stages {
               stage ('stage-1') {
                     steps {
                         /* sh "yum install docker -y"
                           sh "systemctl start docker"*/
                           sh "systemctl status docker"
                           sh "systemctl enable docker"
                     }
                }
                  stage ('stage-2') {
                           steps {
                              sh "docker pull httpd"   
                              sh "docker system prune -a -f"
                              sh "docker run -itdp 90:80 --name 23Q2 httpd"
                              sh "docker cp /mnt/docker/index.html 23Q2:/usr/local/apache2/htdocs"
                           }
                  }
                
          }
}
