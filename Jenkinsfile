#!groovy
@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('Prepare') {
        deleteDir()
        checkout scm
        echo pwd
        setupCommonPipelineEnvironment script:this, runStageInPod: true

    }
    stage('Build') {
        echo pwd
        mtaBuild script: this
    }
}
