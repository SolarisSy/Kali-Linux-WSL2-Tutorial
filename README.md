## Como instalar o Kali Linux via WSL 2 no Windows 11

Este tutorial descreve como instalar o Kali Linux via WSL 2 no Windows 11 e configurá-lo para uso.

### Pré-requisitos
- Windows 11 instalado em seu computador
- Funcionalidade WSL 2 habilitada

### Passo 1 - Habilitar a funcionalidade WSL 2
Siga este [tutorial](https://docs.microsoft.com/en-us/windows/wsl/install-win10#step-1---enable-the-windows-subsystem-for-linux) para verificar e habilitar o WSL 2.

### Passo 2 - Baixar o aplicativo Kali Linux
Procure pelo aplicativo Kali Linux na barra de pesquisa da Microsoft Store e clique em "Instalar".

### Passo 3 - Verificar se o Kali Linux está instalado
Abra o Prompt de Comando do Windows e digite o seguinte comando:
```
$ wsl --list
```
O Kali Linux deve aparecer na lista.

### Passo 4 - Definir o Kali Linux como distribuição padrão do WSL
Digite o seguinte comando no Prompt de Comando:
```
wsl --set-default kali-linux
```
### Passo 5 - Abrir o Kali Linux
Digite "kali" na barra de pesquisa do Windows e selecione "Kali Linux".
ou
Abra o cmd e digite "wsl" se estiver tudo certo seu kali linux deverá inicializar no cmd correspondente

### Passo 6 - Configurar o Kali Linux
Siga este [tutorial](https://www.kali.org/docs/wsl/win-kex/) para configurar o Kali Linux para uso.
Aqui você encontrará uma série de instruções de opções de instalação, gui, versão completa com todas as tools e derivados.

### Passo 7 - Instalar ferramentas adicionais
Use o gerenciador de pacotes apt-get para instalar ferramentas adicionais. Por exemplo, para instalar o Wireshark, digite o seguinte comando no terminal do Kali Linux:
```
sudo apt-get install wireshark
```
### Passo 8 - Acessar arquivos do Windows no Kali Linux
Navegue até a pasta "mnt" do Kali Linux para acessar arquivos do Windows. Por exemplo, para acessar a unidade C do Windows, navegue até "/mnt/c".

### Fontes adicionais
- [Documentação oficial do Kali Linux](https://www.kali.org/docs/)
- [Tutorial sobre como usar o Kali Linux via WSL 2](https://www.youtube.com/watch?v=3q7a-Scnm2Q)
- [Tutorial sobre como instalar ferramentas adicionais no Kali Linux](https://www.kali.org/docs/general-use/install-additional-kali-tools/)
- [Tutorial sobre como compartilhar arquivos entre o Windows e o Kali Linux](https://www.kali.org/docs/wsl/win-kex/#mounting-windows-directories-in-kali-linux-wsl-2)
