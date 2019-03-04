# OS X (Mac)

1. Faca o download da ultima versao do Flutter estavel [aqui](https://storage.googleapis.com/flutter_infra/releases/stable/macos/flutter_macos_v1.2.1-stable.zip "aqui");
2. Extraia o conteúdo .zip para alguma pasta, ela será o caminho da SDK, escolha com cuidado;

# Atualizando o PATH (OS X)
1. Abra (ou crie o arquivo) `$HOME/.bash_profile`. O caminho que esse arquivo se ou o nome pode ser diferente em algumas máquinas;
2. Adicione a seguinte linha e altere o `[CAMINHO_DO_FLUTTER_SDK]` para o caminho onde você baixou a SDK;

	`export PATH="$PATH:[CAMINHO_DO_FLUTTER_SDK]/flutter/bin"`

3. Salve o arquivo e execute `source $HOME/.bashrc_profile` para atualizar a janela atual
4. Verifique se a pasta bin da SDK foi adicionada corretamente com o comando: `echo $PATH`

# iOS Setup

### Instalar Xcode

Para desenvolver para iOS voce precisa ter um Mac com o Xcode 9.0 ou mais novo instalado na sua maquina

1. Insalte o Xcode 9.0 ou mais novo ([Web](https://developer.apple.com/xcode/ "Web") ou [iTunes](https://itunes.apple.com/us/app/xcode/id497799835 "iTunes")).
2. Configure as ferramentas de linha de comandos do Xcode para usar a versão recém-instalada do Xcode executando o seguinte na linha de comando:

	`sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer`

	Obs: Esse é o caminho correto para a maioria dos casos, quando você deseja usar a versão mais recente do Xcode. Se você precisar usar uma versão diferente, especifique esse caminho.

3. Verifique se o contrato de licença do Xcode está assinado, abrindo o Xcode uma vez e confirmando ou executando o `sudo xcodebuild -license` na linha de comando.

# iOS Simulator

1. No seu Mac, localize o Simulador via Spotlight ou usando o seguinte comando:

 	`open -a Simulator`
 
2. Certifique-se de que seu simulador esteja usando um dispositivo de 64 bits (iPhone 5s ou posterior) verificando as configurações no menu **Hardware > Dispositivo** do simulador.

3. Dependendo do tamanho de tela da sua máquina de desenvolvimento, os dispositivos iOS de alta densidade de tela simulados podem transbordar sua tela. Defina a escala do dispositivo no menu **Janela > Escala** no simulador.

# Ferramentas adicionais

1. Instale o [homebrew](https://brew.sh/ "homebrew").
2. Garanta que o homebrew esta atualizado
	`$ brew update`

3. Instale as ferramentas para implantar aplicativos Flutter em dispositivos iOS executando os seguintes comandos:

	`$ brew install --HEAD usbmuxd`  
	`$ brew link usbmuxd`  
	`$ brew install --HEAD libimobiledevice`  
	`$ brew install ideviceinstaller ios-deploy cocoapods`  
	`$ pod setup`  

	Obs: Se algum desses comandos falhar, execute `$ brew doctor` e siga as instruções para resolver qualquer problema.

## Criando e executando seu primeiro projeto

Para criar e testar seus primeiros apps, execute esses comandos:

1. Crie seu primeiro projeto executando essa linha de comando no terminal: 

	`$  flutter create meu_app`

2. Um diretório `meu_app` foi criado, contendo o aplicativo inicial do Flutter. Entre neste diretório: 

	`$  cd my_app`

3. Para iniciar o aplicativo no Simulador, assegure-se de que o Simulador esteja em execução e execute no terminal:

	`$ flutter run`
