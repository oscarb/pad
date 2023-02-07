---
title: Visual Studio Code
tags:
  - apps
published: true
---

# Visual Studio Code

https://code.visualstudio.com/

## Keymaps

[IntelliJ IDEA Keybindings](https://marketplace.visualstudio.com/items?itemName=k--kato.intellij-idea-keybindings)

## Color Theme

* Arc Dark

## Code


## Insiders

**Code** (Mac OS)
```json
{
    "workbench.activityBar.visible": true,
    "workbench.statusBar.visible": true,
    "workbench.colorTheme": "One Dark Pro Vivid",
    "editor.minimap.enabled": false
}
```



## Remote work

### SMB

Open files from SMB folders just as if they're local files. Comes with bad performance.

### code-server

Open source VS Code server that can be self-hosted and accessed over HTTP as a website. 

Features:
* Password protection
* Proxy web ports
* Certificate support
* Plugin API

Availale docker containers:
 * [linuxserver/code-server](https://hub.docker.com/r/linuxserver/code-server) 
 	* Supports docker mods
 	* "It offers more flexibility and customization than the coder release. "
 * [codercom/code-server](https://registry.hub.docker.com/r/codercom/code-server/) - official
 
[Source](https://coder.com/docs/code-server/latest/FAQ#whats-the-difference-between-code-server-and-openvscode-server)

### OpenVScode server

Another open source VS Code that can be self-hosted accessed over HTTP as a website.

* Scoped at only making VS Code available in the web browser
* Faster updates 
* Reduce menu bar

### VS Code server

Offical self-hosted server, closed source and accessed through tunneling. 

### SSH 

Access files over SSH from local VS Code.

### GitHub Codespace

#### Web

Access a GitHub repository on a powerful remote machine through a webpage.

#### Local

Access a GitHub repository on a powerful remote machine through your local VS Code setup.

### Tunnel 

Access your local VS Code through a tunnel. 


### vscode.dev

Browser-hosted VS Code.


### Remote repositories 

Open GitHub repositories as if they were local folders.