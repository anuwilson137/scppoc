@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('prepare') {
        checkout([$class: 'GitSCM', branches: [[name: "${params.GIT_BRANCH}"]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'SAP-cloud-Poc',url: "git@github.pie.apple.com:scppoc/scpdevopssample.git"]]])
        setupCommonPipelineEnvironment script:this
    }
    stage('build') {
        //mtaBuild script: this
    }
    stage('deploy') {
        //cloudFoundryDeploy script: this
    }
}
