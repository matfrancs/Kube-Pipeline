node {

   stage 'Stage 1'
   echo 'Hello World 1'

   stage 'Stage 2'
   echo 'Hello World 2'

   stage 'Checkout'
    /* Checkout the code we are currently running against */
    checkout scm

   stage 'Run app on Kubernetes'
#    withKubernetes( serverUrl: 'https://kube.univision.com', credentialsId: 'kube-aws-kube-global2-admin' ) {
#          sh 'kubectl get pods'
#    }
   wrap([$class: 'KubectlBuildWrapper', serverURL: 'https://kube.univision.com', credentialsId: 'kube-aws-kube-global2-admin' ]) {
       sh 'kubectl get pods'
     } 

    }
