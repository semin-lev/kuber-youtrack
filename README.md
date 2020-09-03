# Youtrack helm chart 


## Create Pod
Install to default namespace: 
`helm install <name> .`

Install to namespace:
`helm install <name> . -n <namespace>`

## Get access token
Youtrack will ask you to finalize the setup. To get authentication token:

  - ssh into a pod shell `kubectl exec --stdin --tty <podname> -- /bin/bash`
  - Grab token `cat /opt/youtrack/conf/internal/services/configurationWizard/wizard_token.txt`

Use this to complete configuration. 

## Remove Pod
`helm delete <name> -n <namespace>` 

