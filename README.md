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