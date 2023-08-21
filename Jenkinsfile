pipeline {
  agent any
  stages {
    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('fetch code') {
      steps {
        git(url: 'git@github.com:Ishabagga/simplilearn-blueocean.git', branch: 'main')
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}