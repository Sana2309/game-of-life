pipeline {
  agent any

  stages {

    stage('Clone Code') {
      steps {
        git 'https://github.com/Sana2309/game-of-life.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t game-of-life gameoflife-acceptance-tests/'

      }
    }

    stage('Terraform Init') {
      steps {
        sh 'cd terraform && terraform init'
      }
    }

    stage('Terraform Apply') {
      steps {
        sh 'cd terraform && terraform apply -auto-approve'
      }
    }
    stage('Debug') {
    steps {
        sh 'pwd'
        sh 'ls -R'
    }
}
  }
}
  }
}
