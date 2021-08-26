pipeline{
    agent { label "master" }
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
                ansible-playbook -i hosts -vv httpd.yml
                
                '''
            }
        }
        
    }
}