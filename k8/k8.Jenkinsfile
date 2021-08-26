pipeline{
    agent { label "piserver" }
    stages{
        /*stage("git-checkout"){
            steps{
                sh '''
                git clone https://github.com/newbielinux1/docker-nginx.git
                '''
            }
        }*/
        stage("ansible-run"){
            steps{
                sh '''
                cd k8
                kubeclt delete -f nginx-deploy.yml | exit 0
                kubeclt apply -f nginx-deploy.yml

                #/root/.kube/config
                
                
                '''
            }
        }
        
    }
}