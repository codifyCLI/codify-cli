# Codify

Welcome to Codify, your go-to solution for managing macOS developer dependencies
using a configuration as code approach. Codify empowers developers to install
dependencies and configure applications in a stable and reproducible manner.

Example config:

```json
[
  {
    "type": "homebrew",
    "formulae": ["jq", "openjdk@17", "jenv", "docker"],
    "casks": ["sublime-text", "dbeaver-community", "intellij-idea-ce"]
  },
  { 
    "type": "nvm",
    "nodeVersions": [
      "12.22",
      "20.8"
    ],
    "global": "20.8"
  }
]
```
This will install homebrew, nvm (Node version manager) plus some useful tools. The cool thing is, if anything has already installed, 
Codify is smart enough exclude those things from the installation. It can also figure out configuration differences between what is
specified versus what is currently on the system. 

**Download**: https://docs.codifycli.com/getting-started/installation/
