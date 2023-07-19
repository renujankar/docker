pipeline {
      agent { 
          label 'dev'
      }
          stages {
               stage ('stage-1') {
                     steps {
                         // sh " sudo yum install docker -y"//
                           sh "sudo systemctl start docker"
                           sh "sudo systemctl status docker"
                           sh "sudo systemctl enable docker"
                     }
                }
                  stage ('stage-2') {
                           steps {
                             // sh "sudo yum install git -y"//
                              //sh "sudo git clone https://github.com/renujankar/docker.git"//
                              //sh "sudo cd "//
                              //sh "sudo docker pull httpd"//
                              /*sh "sudo docker stop 23Q1-1"
                              sh "sudo docker rm 23Q1-1"*/
                              sh "sudo docker system prune -a -f"
                              sh "sudo docker run -itdv /mnt:/usr/local/apache2/htdocs httpd "
                              sh "sudo docker run -itdp 8000:80 --name 23Q1-1 httpd"
                              sh "sudo docker cp index.html 23Q1-1:/usr/local/apache2/htdocs"
                              sh "sudo docker exec 23Q1-1 chmod -R 777 /usr/local/apache2/"
                           }
                  }
                
          }
}

