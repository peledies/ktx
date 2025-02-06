# KTX
A kubernetes context and kubectl switcher

```
██╗  ██╗████████╗██╗  ██╗
██║ ██╔╝╚══██╔══╝╚██╗██╔╝
█████╔╝    ██║    ╚███╔╝
██╔═██╗    ██║    ██╔██╗
██║  ██╗   ██║   ██╔╝ ██╗
╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝
Kubectl Context Switcher
```

## Installation
*Install with homebrew*

```
brew tap peledies/formulae

brew install ktx
```

## Configuration
`Ktx` requires a few modifications to your profile to work effectively.

### PATH
Add the following lines to your profile `~/.bash_profile`, `~/.bashrc` or `~/.zshrc`
> This tells your system where your `ktx` installed versions of `kubectl` reside
```
# Kubectl versions installed with ktx
PATH=$HOME/.kube/kubectl:$PATH
```

> This loads `ALL` kubernetes config files into memory so `ktx` can build its menu
```
# Load all the config files in the .kube directory
export KUBECONFIG=$(find ~/.kube -name 'config*' | sort | tr '\n' ':')
```

## LastPass Integration
1. Create a new custom type in Lastpass.

<img src="/img/lp1.png" width="500" />


2. Name it `Kubernetes-Config-Raw` and make sure it has a single `notes` field.

<img src="/img/lp2.png" width="500" />


3. Create a new `Kubernetes-Config-Raw` record and name it something useful to you. Put the contents of your kube config for that single cluster in the `Notes` input.

<img src="/img/lp3.png" width="500" />


4. Make sure your `Kubernetes-Config-Raw` records are in the `kubernetes-configs` (all lowercase) folder.

<img src="/img/lp4.png" width="500" />