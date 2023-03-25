## Como instalar o Kali Linux via WSL 2 no Windows 11

Este tutorial descreve como instalar o Kali Linux via WSL 2 no Windows 11 e configurá-lo para uso.

### Pré-requisitos
- Windows 11 instalado em seu computador
- Funcionalidade WSL 2 habilitada

## Passo 1 - Habilitar a funcionalidade WSL 2
Para Habilita a funcionalidade WSL 2 você pode seguir este [tutorial](https://docs.microsoft.com/en-us/windows/wsl/install-win10#step-1---enable-the-windows-subsystem-for-linux) para verificar e habilitar o WSL 2 diretamente da Microsoft Windows ou seguir com nosso tutorial propriamente para *Kali linux*


Antes de começar o tutorial, é importante mencionar que o WSL 2 (Windows Subsystem for Linux 2) é uma tecnologia disponível no Windows 10 versão 2004 ou superior e no Windows 11. Além disso, é necessário ter habilitada a virtualização no BIOS do computador para usar o WSL 2.

Aqui está um tutorial detalhado sobre como ativar o WSL 2:

### Primeiro: Verifique a versão do Windows

Antes de tudo, é importante verificar a versão do Windows que você está usando. Para isso, siga os passos abaixo:

1.1. Abra o menu Iniciar do Windows e digite "winver" na barra de pesquisa.
1.2. Selecione o resultado "winver - Verificar a versão do Windows".

Uma janela com a versão do Windows será exibida. Verifique se a versão é 2004 ou superior para continuar com este tutorial.

Passo 2: Habilite o recurso "Plataforma de Subsistema do Windows"

O WSL 2 requer a "Plataforma de Subsistema do Windows" habilitada no Windows. Para fazer isso, siga os passos abaixo:

2.1. Abra o menu Iniciar do Windows e digite "Recursos do Windows" na barra de pesquisa.
2.2. Selecione o resultado "Ativar ou desativar recursos do Windows".
2.3. Role para baixo na lista de recursos e localize "Plataforma de Subsistema do Windows".
2.4. Selecione a caixa de seleção ao lado de "Plataforma de Subsistema do Windows" e clique em OK.

Passo 3: Atualize o kernel do WSL 2

O WSL 2 requer um kernel atualizado para funcionar corretamente. Para atualizar o kernel do WSL 2, siga os passos abaixo:

3.1. Abra o PowerShell como administrador. Para isso, abra o menu Iniciar do Windows, digite "PowerShell" na barra de pesquisa, clique com o botão direito do mouse no resultado "Windows PowerShell" e selecione "Executar como administrador".
3.2. No PowerShell, execute o seguinte comando:
```
wsl --set-default-version 2
```
Este comando define a versão padrão do WSL como WSL 2.

3.3. Em seguida, execute o seguinte comando para baixar e instalar a atualização do kernel do WSL 2:
```
wsl --update
```
Aguarde até que o processo de atualização seja concluído.

## Pronto agora você tem a wsl 2 configurada e pronta para a instalação do seu Kali Linux

## Passo 2 - Baixar o aplicativo Kali Linux
Primeiro em seu cmd passe o seguinte comando
```
wsl --list --onlie
```
Procure o aplicativo com o nome de kali-linux, verifique se essa é a distruição desejada
agora só instalar
para instalar você primeiro vai precisar passar o comando de instalação na sua máquina da distruição com o seguinte comando:
```
wsl --install -d <Distribution Name>
```
nesse caso:
```
wsl --install -d kali-linux
```
ou você pode optar por instalar o aplicativo Kali Linux na barra de pesquisa da Microsoft Store e clique em "Instalar".

## Passo 3 - Verificar se o Kali Linux está instalado
Abra o Prompt de Comando do Windows e digite o seguinte comando:
```
wsl --list
```
O Kali Linux deve aparecer na lista.

## Passo 4 - Definir o Kali Linux como distribuição padrão do WSL
Digite o seguinte comando no Prompt de Comando:
```
wsl --set-default kali-linux
```
## Passo 5 - Abrir o Kali Linux
Digite "kali" na barra de pesquisa do Windows e selecione "Kali Linux"
ou
Abra o cmd e digite "wsl" se estiver tudo certo seu kali linux deverá inicializar no cmd correspondente

## Passo 6 - Configurar o Kali Linux
Siga este [tutorial](https://www.kali.org/docs/wsl/win-kex/) para configurar o Kali Linux para uso.
Aqui você encontrará uma série de instruções de opções de instalação, gui, versão completa com todas as tools e derivados.

## Passo 7 - Instalar ferramentas adicionais
Use o gerenciador de pacotes apt-get para instalar ferramentas adicionais. Por exemplo, para instalar o Wireshark, digite o seguinte comando no terminal do Kali Linux:
```
sudo apt-get install wireshark
```
## Passo 8 - Acessar arquivos do Windows no Kali Linux
Navegue até a pasta "mnt" do Kali Linux para acessar arquivos do Windows. Por exemplo, para acessar a unidade C do Windows, navegue até "/mnt/c".

### Fontes adicionais
- [Documentação oficial do Kali Linux](https://www.kali.org/docs/)
- [Tutorial sobre como usar o Kali Linux via WSL 2](https://www.youtube.com/watch?v=o1_E4PBl30s)
- [Tutorial sobre como instalar ferramentas adicionais no Kali Linux](https://www.kali.org/tools/)
- [Tutorial sobre como compartilhar arquivos entre o Windows e o Kali Linux](https://www.kali.org/docs/wsl/win-kex/#mounting-windows-directories-in-kali-linux-wsl-2)
