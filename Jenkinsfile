node{

    stage('SCM Checkout')
    {
        git credentialsId: '549121b5-6f7d-4571-88b3-d43091beddf0', url: 'https://github.com/Aditi2020/online-shop'
    }
    
    stage('Run Docker Compose File')
    {
        'docker-compose build'
        'docker-compose up -d'
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
             
             sh 'sudo docker login -u "aditi1305" -p "@Pass0510" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push aditi1305/firstimage'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
