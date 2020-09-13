pipeline {
	agent any
	stages {
		stage('Build'){
			steps{
					pdflatex resume.tex
			}
		}
		stage('Move to website'){
			steps{
				mv resume.pdf ~/Documents/rzhou10.github.io/src/pdfs
				cd ../rzhou10.github.io
				bash deploy.sh
			}
		}
	}
}