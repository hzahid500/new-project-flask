pipeline {
  agent any
  stages {
    
    stage("GIT CHECKOUT") {
      steps {
        echo "cloning the git repo"
        git branch: "main", url: "https://github.com/hzahid500/flask-app-deployment.git"
      }
    }

    stage("BUILD") {
      steps {
        echo "building the docker image"
        sh "docker build -t flask-app:v1.0 ."
      }
    }
  }
}
