### Installation steps

To install helm operater, flux, and argocd to a new cluster use the following steps:

1. Install base flux, helm, and helm operator: 
`kubectl -k install/prod`
2. Get ssh-key generated by flux:
 `fluxctl -n flux-system identity`
3. Add ssh key to deploy keys (bitbucket, gitlab, github, etc) with write access

