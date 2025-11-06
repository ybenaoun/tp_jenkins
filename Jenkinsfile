pipeline {
  agent any
  options { timestamps() }
  stages {
    stage('Cloner le dépôt') {
      steps {
        git url: 'https://github.com/ybenaoun/tp_jenkins.git', branch: 'master'
      }
    }
    stage('Étape 1 : Vérification du dépôt') {
      steps {
        bat 'echo === Étape 1 : Vérification du dépôt ==='
        bat 'git status'
      }
    }
    stage('Étape 2 : Afficher le contenu du projet') {
      steps {
      bat 'echo === Étape 2 : Afficher le contenu du projet ==='
      bat 'dir'
      }
    }
    stage('Étape 3 : Simuler un déploiement local') {
      steps {
        bat 'echo === Étape 3 : Simuler un déploiement local ==='
        bat 'echo Le fichier index.html est prêt à être affiché'
      }
    }
    stage('Étape 4 : Fin du build') {
      steps {
        bat 'echo === Étape 4 : Fin du build ==='
        bat 'echo SUCCESS'
      }
    }
  }
  post {
    success { echo ' Build OK' }
    failure { echo ' Build KO' }
  }
}
pipeline {
agent any
stages {
stage('Docker') {
steps {
bat 'whoami'
bat 'docker version'
bat 'docker run --rm nginx:alpine nginx -v'
}
}
}
}
