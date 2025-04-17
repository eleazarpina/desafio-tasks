pipeline {
  agent any

  stages {
    stage('Clonar Repositorio') {
      steps {
        git url: 'https://github.com/eleazarpina/desafio-tasks', branch: 'main'
      }
    }
    stage('Instalar Dependencias') {
      steps {
        bat 'npm install'
      }
    }
    stage('Ejecutar Pruebas') {
      steps {
        bat 'npm run test'
      }
    }  
    stage('Creacion contenedores') {
      steps {        
        bat 'docker build -t task-api .'
      }
    }
  }
}