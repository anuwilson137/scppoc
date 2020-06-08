#!groovy
@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('prepare') {
        deleteDir()
        checkout scm
        echo readYaml(text: "---")
      //  def data = readYaml file: 'mta.yaml'
        setupCommonPipelineEnvironment script:this
        echo pwd
        sh "ls"
    }
    stage('build') {
        echo pwd
        sh "ls"
        mtaBuild script: this
    }
}
