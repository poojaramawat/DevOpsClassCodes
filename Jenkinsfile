pipeline {
    agent any
  tools {
    jdk 'myjava'
    maven 'mymaven'
  }
  stages {
      stage('Clonerepo') {
         steps {
            git 'https://github.com/poojaramawat/DevOpsClassCodes.git'
         }
      }
      stage('mavencompile') {
         steps {
            sh 'mvn compile'
         }
      }
      stage('CodeReview') {
         steps {
            sh 'mvn pmd:pmd'
         }
      }
      stage('Unit-test') {
         steps {
            sh 'mvn test'
         }
      }

  }
}
