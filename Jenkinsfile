node{

    stage('SCM Checkout')
    {
        git credentialsId: 'jenkins_war', url: 'https://github.com/anandreddy143/Online-retail.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "docker3125" -p "sree@3125" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push docker3125/myfile_1'
             sh 'sudo docker push docker3125/myfile_1'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
