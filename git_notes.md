# GIT & GitHub

## GIT Bash
- **Git clone** vytvoří přímou (tupou) kopii adresáře z remote v lokálním pracovním prostoru.
- **Git pull** (**git fetch**, **git merge**) provádí update lokálního adresáře doplněním nových commitů.
  - *git pull runs git fetch with the given parameters and then depending on configuration options or command line flags, will call either git rebase or git merge to reconcile diverging branches.*
- **Git push** odesílá lokální změny z konkrétní branche na remote server (origin).

### Klonování repo
- přejít do adresáře s repositáři (otevřít odtamtud git bash)
  - `git clone git@github.com:wladas92/my_repo_name.git`

### Nahrání na server
- přejít do adresáře s konkrétní repo (otevřít odtamtud git bash)
- přidám soubory (*-A* zapracuje všechny změny včetně delete)
  - `git add -A`
- provedu commit (*-m* je message)
  - `git commit -m TEST`
- sloučený příkaz přes .bash_profile alias (`git add -A && git commit -m $2`)
  - `gaacom TEST`
- synchronizuji složky (*origin* = remote, *main* = branch)
  - `git push origin main`

### Synchronizace lokálního adresáře
- (ve většině případů) použiju pull
  - `git pull`

***

## SSH (nová konfigurace)
### Vytvořím SSH key
> `$ ssh-keygen -t ed25519 -C "opolskyvlada@gmail.com"`

<details>
  <summary>Response</summary>

```
Your identification has been saved in /c/Users/opols/.ssh/id_ed25519
Your public key has been saved in /c/Users/opols/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:pfcVWs8ZAJfR28kbmN0jVSEc2suZndvgTZ01o28M8x8 opolskyvlada@gmail.com
The key's randomart image is:
+--[ED25519 256]--+
|           .o*=.+|
|            +ooo |
|          .. .O+*|
|         o  .**@%|
|        S . .O+=O|
|         . . o*=o|
|            . .Eo|
|              . o|
|                .|
+----[SHA256]-----+
```

</details>

### Nastartuji (manuálně) SSH-Agent
> `eval "$(ssh-agent -s)"`

### Přidám SSH key do agenta
> `ssh-add ~/.ssh/id_ed25519`

### Přidám SSH klíč do profilu na Github.com
*Viz postup v [dokumentaci](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)*

### Test spojení
> `ssh -T git@github.com`

*Hi wladas92! You've successfully authenticated, but GitHub does not provide shell access.*

### Autostart SSH (check při spuštění Git Bash)
Vytvořen file **~/.bash_profile** obsahující autostart SSH agenta (*viz postup v [dokumentaci](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases#auto-launching-ssh-agent-on-git-for-windows)*), aliasy a další užitečné hovadiny. 

