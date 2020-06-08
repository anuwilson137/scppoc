#!groovy
@Library('piper-lib-os') _
    stage('prepare') {
        node('BuildAgent-001') {
        deleteDir()
        checkout scm
      //  echo readYaml(text: "---")
      //  def data = readYaml file: 'mta.yaml'
        setupCommonPipelineEnvironment script:this
        echo pwd
        sh "ls"
        }
    }
    stage('build') {
        node('BuildAgent-001') {
        mtaBuild script: this
    }
}
