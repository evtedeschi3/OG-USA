node {
    withCredentials([[$class: 'StringBinding', credentialsId: 'OSPC_API_KEY', variable: 'OSPC_API_KEY']]) {

        sh '''echo About to checkout scm'''
        checkout scm
        sh '''echo Checked out scm'''
        sh '''env | sort && echo pwd is `pwd` && ls -alRth . .. ../.. $WORKSPACE | sort && cd Python/regression
        bash run_reforms_bash.sh'''
    }
}
