# OS X (Mac)

1. Faca o download da ultima versao do Flutter estavel [aqui](https://storage.googleapis.com/flutter_infra/releases/stable/macos/flutter_macos_v1.2.1-stable.zip "aqui");
2. Extraia o conteúdo .zip para alguma pasta, ela será o caminho da SDK, escolha com cuidado;

# Atualizando o PATH (OS X)
1. Abra (ou crie o arquivo) `$HOME/.bash_profile`. O caminho que esse arquivo se ou o nome pode ser diferente em algumas máquinas;
2. Adicione a seguinte linha e altere o `[CAMINHO_DO_FLUTTER_SDK]` para o caminho onde você baixou a SDK;

 `export PATH="$PATH:[CAMINHO_DO_FLUTTER_SDK]/flutter/bin"`

3. Salve o arquivo e execute `source $HOME/.bashrc_profile` para atualizar a janela atual
4. Verifique se a pasta bin da SDK foi adicionada corretamente com o comando: `echo $PATH`
