pipeline {
  agent any
  tools {nodejs "NODEJS"}
  tools {docker "DOCKER"}
  stages {
    stage('Clonar Repositorio') {
      steps {
        git url: 'https://github.com/eleazarpina/desafio-tasks', branch: 'main'
      }
    }
    stage('Instalar Dependencias') {
      steps {
        sh 'npm install'
      }
    }
    stage('Creacion contenedores') {
      steps {        
        sh 'docker build -t task-api .'
      }
    }
  }
}