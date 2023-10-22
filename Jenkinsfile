pipeline {
    agent any
    stages {
        stage('install docker') {
            steps {
                sudo dnf update
                sudo dnf install docker -y
                sudo systemctl start docker
                sudo systemctl enable docker
                sudo usermod -a G docker ec2-user
                newgrp docker
            }
        }
    }
}
