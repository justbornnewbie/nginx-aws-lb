pipeline{
    agent { label "worker1" }
    stages{
        /*stage("git-checkout"){
            steps{
                sh '''
                git clone https://github.com/newbielinux1/docker-nginx.git
                '''
            }
        }*/
        stage("terraform-setup"){
            steps{
                sh '''
                cp /opt/creds/key.pub ./nginx-lb
                cd nginx-lb
                terraform init
                terraform plan
                terraform apply -auto-approve
                
                '''
            }
        }
        
    }
}