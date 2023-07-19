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
                             // sh "docker pull httpd"//
                             // sh "sudo docker stop 23Q2-2"//
                             // sh "sudo docker rm 23Q2-2"//
                              sh "sudo docker system prune -a -f"
                              sh "sudo docker run -itdv /mnt:/usr/local/apache2/htdocs httpd "
                              sh "sudo docker run -itdp 8082:80 --name 23Q2-2 httpd"
                              sh "sudo docker cp index.html 23Q2-2:/usr/local/apache2/htdocs"
                              sh "sudo docker exec 23Q2-2 chmod -R 777 /usr/local/apache2/"
                           }
                  }
                
          }
}
