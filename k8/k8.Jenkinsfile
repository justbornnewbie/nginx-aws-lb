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
                kubectl delete -f nginx-deploy.yml | exit 0
                kubectl apply -f nginx-deploy.yml

                #copy k8master config file to piserver:/root/.kube/config

                
                '''
            }
        }
        
    }
}