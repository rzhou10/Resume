#!/usr/bin/env groovy
pipeline {
  agent any

  stages {
    stage('Build'){
      steps{
        pdflatex resume.tex
        echo 'Resume built'
      }
    }

    stage('Move to website repo'){
      steps{
        mv resume.pdf ~/Documents/rzhou10.github.io/src/pdfs
        cd ../rzhou10.github.io
        echo 'Moved resume to website code'
      }
    }

    stage('Deploy website'){
      steps{
        bash deploy.sh
        echo 'Deployed website'
      }
    }
  }
}
