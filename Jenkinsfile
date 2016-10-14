node {

   stage 'Stage 1'
   echo 'Hello World 1'

   stage 'Stage 2'
   echo 'Hello World 2'

   stage 'Checkout'
    /* Checkout the code we are currently running against */
    checkout scm

   stage 'Run app on Kubernetes'
       sh 'kubectl get pods --namespace jenkins'
       sh 'kubectl get services --namespace jenkins'

    }
