node {
    stage('SCM') {
		git changelog: false, poll: false, url: 'https://github.com/98amanmaurya/SSIS.git'
    }
    stage('Database schema upgrade') {
        echo 'Upgrading target schema'
    }
    stage('Execute Package') {
		bat label: 'Executing package', script: 'dtexec /f FirstSSISPackage.dtsx'
    }
 }
