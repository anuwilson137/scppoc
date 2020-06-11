#!groovy
//import com.sap.piper.Utils
//import com.sap.piper.ConfigurationLoader
//import com.sap.piper.ConfigurationMerger
@Library('piper-lib-os@master') _
node('BuildAgent-001') {
    stage('prepare') {
        cleanWs()
        deleteDir()
        checkout scm
        echo readYaml(text: "---")
      //  def data = readYaml file: 'mta.yaml'
   //     echo pwd
        setupCommonPipelineEnvironment script: this
        //piperPipeline script: this, runStageInPod: true
        echo pwd
        sh "ls -la ${pwd()}"
     //   sh "ls -ltr /ngs/app/sapopsd/jenkins-agent-home/workspace/Build-SCP-template-application/"

    }
    stage('build') {
        echo "-----------------------------------------------------------------"
        echo pwd
        sh "ls -la ${pwd()}"
        mtaBuild script: this

    }
}

