### Installation steps

To install helm operater, flux, and argocd to a new cluster use the following steps:

1. Install base flux, helm, and helm operator: 
`kubectl -k install/prod`
2. Install tiller (will be removed with helm3 support) 
`helm init --service-account tiller --history-max 10`
3. Get ssh-key generated by flux:
 `fluxctl -n flux-system identity`
4. Add ssh key to deploy keys (bitbucket, gitlab, github, etc) with write access