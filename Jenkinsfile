pipeline {
      agent 
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
                              //sh "docker pull httpd"// 
                              /*sh "docker stop 23Q3"
                              sh "docker rm 23Q3"*/
                              sh "docker system prune -a -f"
                              sh "docker run -itd --name 23Q3 -p 8081:80 -v /mnt:/usr/local/apache2/htdocs httpd"
                             // sh "docker run -itdp 8083:80 --name 23Q3-3 httpd"//
                              sh "docker cp index.html 23Q3:/usr/local/apache2/htdocs"
                              sh "docker exec 23Q3 chmod -R 777 /usr/local/apache2/"
                           }
                  }
                
          }
}
