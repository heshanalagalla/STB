node{

    stage('SCM Checkout')
    {
        git credentialsId: 'c0f25342077edc0e344cd8820e6f11787946a0d3', url: 'https://github.com/heshanalagalla/STB.git'
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
             
             sh 'sudo docker login -u "heshanalagalla" -p "Mkj9rXLrT9CrN2N" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push heshanalagalla/stbb'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
