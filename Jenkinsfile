pipeline {
      agent {
          label 'dev'
      }
          stages {
               stage ('stage-1') {
                     steps {
                         /* sh "yum install docker -y"
                          sh "systemctl start docker"*/
                           sh "sudo systemctl status docker"
                           //sh "systemctl enable docker"//
                     }
                }
                  stage ('stage-2') {
                           steps {
                              //sh "docker pull httpd"// 
                              /*sh "docker stop 23Q3"
                              sh "docker rm 23Q3"*/
                              sh "sudo docker system prune -a -f"
                              sh "sudo docker run -itdv /mnt:/usr/local/apache2/htdocs httpd"
                              sh "sudo docker run -itdp 8083:80 --name 23Q3-3 httpd"
                              sh "sudo docker cp index.html 23Q3-3:/usr/local/apache2/htdocs"
                              sh "sudo docker exec 23Q3-3 chmod -R 777 /usr/local/apache2/"
                           }
                  }
                
          }
}
