<h2>🪟  WINDOWS</h2>
<h4>INSTALAÇÃO OPENJDK 17.0.4+8 Azul Zulu</h4>
<ol>
<li><a href="https://cdn.azul.com/zulu/bin/zulu17.36.19-ca-jdk17.0.4.1-win_i686.zip">Entre no site oficial da Azul</a></li>
<li>Faça o Download do arquivo <a href="https://cdn.azul.com/zulu/bin/zulu17.36.13-ca-jdk17.0.4-linux_x64.zip">.zip</a> (Azul Zulu: 17.0.4+8 x86 64-bit)
</li>
<li>No seu Computador: Vá no Drive -> C://Arquivo de Programas</li>
<li>Caso não tenha um diretório com o nome Java, crie</li>
<li>Entre neste diretório e descompacte o download do zip JDK Azul Zulu 17.0.4+8 neste diretório</li>
<li>Copie caminho do diretório que você descompactou o zip JDK Azul Zulu 17.0.4+8</li>
<li>Configuração de ambiente <code>JAVA_HOME</code>:</li>
<ol>
<li>Menu iniciar >> Editar as varáveis de ambiente do sistema</li>
<li>Irá abrir a janela Propriedades do Sistema, escolha a aba Avançado, em seguida clique em variáveis de Ambiente</li>
<li>Na janela Variáveis de Ambiente,  crie um novo Variáveis do sistema</li>
<li>Abrirá uma janela: Nova Variável de Sistema</li>
<li>Nome da variável: <code>JAVA_HOME</code></li>
<li>Valor da variável: Cole o caminho do diretório que você descompactou o zip JDK Azul Zulu 17.0.4+8 >> Ok</li>
<li>Na mesma janela Variáveis do Sistema, localize a variável Path, selecione e clique a opção Editar...</li>
<li>Clique na opção Novo e cole o mesmo caminho que você descompactou o JDK Azul Zulu 17.0.4+8 acrescentando <code>\bin</code></li>
<li>Continue com o Path selecionado e clique na opção Mover para Cima até chegar no topo</li>
</ol>
<li>Abra o Prompt de Comando: Menu iniciar >> cmd</li>
<li>Execute: <code>java --version</code></li>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>
<p align="right"><em>Créditos: <a href="https://www.youtube.com/watch?v=laC0fiI-IOM">DevSuperior</a></em></p>

<h4>INSTALAÇÃO GIT</h4>
<ol>
<li><a href ="https://git-scm.com/downloads">Entre no site oficial do GIT</a></li>
<li>Escolha a opção Windows e o instalador será baixado automáticamente</li>
<li>Mantenha as opções pré selecionadas</li>
<li>Next</li>
<li>Install</li>
<li>Antes de finaizar a instalação, selecione a opção "Lauch Git Bash"</li>
<li>No Git Bash, verifique se o GIT está instalado: <code>git --version</code></li>
<li>Configurações iniciais:
<ol>
<li>Configurar o nome de usuário: <code>git config --global user.name "Seu nome"</code></li>
<li>Configurar o endereço de e-mail (o mesmo do GitHub): <code>git config --global user.email seu_email_do_GitHub@email.br</code>
</li> 
<li>Verifique as configurações: <code>git config --list</code></li>
</ol>
</li>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>

<h4>GERAR ACCESS TOKEN</h4>
<ol>
<li>Faça seu login no GitHub</li>
<li><a href="https://github.com/settings/tokens/new">Gere um access token</a>: Your Profile >> Settings >> Developer settings >> Personal access tokens >> Generate new token 
<ol>
<li>Note: Ecolha um nome para o token</li>
<li>Expiration: No expiration</li>
<li>Select scopes: Selecione todos os campos</li>
<li>Generate token</li>
</ol>
</li>
<li>Copie a String referente ao token</li> 
<li>Aalve em um lugar seguro que você consiga consultar posteriormente</li>
<li>Criação e configurações iniciais concluídas!</li>
</ol>

<h4>GERAR SSH KEY</h4>
<ol>
<li>Consulte a <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh">documentação oficial</a></li>
<li>Verifique se <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys">existe alguma SSH key</a> na sua máquina: 
<ol>
<li>No Git Bash: <code>ls -al ~/.ssh</code></li>
<li>Se sim, para ser válido, o GitHub suporta qualquer um desses nomes de arquivos a seguir:
<ul>
<li>id_rsa.pub</li>
<li>id_ecdsa.pub</li>
<li>id_ed25519.pub</li>
</ul>
</li>
</ol>
<li>Caso não exista, <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent">gere uma SSH key</a>:
<ol>
<li>No Git Bash: <code>ssh-keygen -t ed25519 -C "seu_email_do_GitHub@example.com"</code></li>
<li>Caso a <em>opção acima não funcione</em>: <code>ssh-keygen -t rsa -b 4096 -C "seu_email_do_GitHub@example.com"</code></li>
<li>Pressione Enter</li>
<li>Pressione Enter</li>
<li>Pressione Enter</li>
</ol>
</li>
<li><a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account">Adicione a nova SSH key na sua conta do GitHub</a>:
<ol>
<li>No Git Bash: Copie o conteúdo do arquivo id_ed25519.pub: <code>clip < ~/.ssh/id_ed25519.pub</code></li>
<li><a href="https://github.com/settings/keys">No GitHub</a>: Your Profile >> Settings >> SSH and GPG keys >> New SSH key
<li>Cole o conteúdo da chave pública</li>
</ol>
<li>Teste a conexão SSH: 
<ol>
<li>No Git Bash: <code>ssh -T git@github.com</code></li>
<li><code>yes</code></li>
</ol>
</li>
<li>Criação e configurações iniciais concluídas!</li>
</ol>

<h4> INSTALAÇÃO INTELLIJ IDEA COMMUNITY </h4>
<ol>
<li>Entre no <a href="https://www.jetbrains.com/idea/download/#section=windows">site da Jetbrains</a></li>
<li>Escolha a opção Community e faça o Download</li>
<li>Siga com Next</li>
<li>Installation Options:
<ol>
<li>64-bit launcher (caso seu sistema seja 64-bit, caso não, selecione 32-bit)</li>
<li>Add "Open Folder as Project"</li>
<li>.java - .groovy - .kt - .kts</li>
<li>Add lauchers dir to the PATH</li>
<li>Next</li>
</ol>
</li>
<li>Install</li>
<li>Para finalizar a instalação, escolha a opção Reebot later</li>
<li>Configurações Iniciais:</li>
<ol>
<li>Aceite os termos: I confirm that I have... >> Confirm</li>
<li>Data Sharing >> Send Anonymous Statistics</li>
</ol>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>
<hr>

<h2>🐧 LINUX - UBUNTU</H2>
<h4>INSTALAÇÃO OPENJDK 17</h4>
<ol>
<li>Abra o terminal (Ctrl + Alt + t)</li>
<li>Verifique se você tem o Java instalado: <code> java --version </code </li>
<li>Caso não, instale: <code> sudo apt-get install openjdk-17-jdk</code></li>
<li>Verifique se o Java realmente foi instalado e em qual caminho:
<ol>
<li><code>java --version</code></li>
<li><code>sudo update-alternatives --config java</code></li>
</ol>
<li>Copie e guarde o caminho de instalação do Java, no meu caso: <code>/usr/lib/jvm/java-17-openjdk-amd64/bin/java</code></li>
<li>Configure a variável em ambiente <code>JAVA_HOME</code>:</li>
<ol>
<li>Abra o arquivo de configuração .bashrc. (Vou utilizar o editor gedit): <code>sudo gedit ~/.bashrc</code></li>
<li>Copie o código abaixo e cole no final do arquivo .bashrc (Observe o caminho do JAVA_HOME):<br>
<code>JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64</code><br>
<code>export JAVA_HOME</code><br>
<code>export PATH=$PATH:$JAVA_HOME</code>
</li>
<li>Salve o arquivo .bashrc</li>
</ol>
<li>Confira se as configurações foram salvas: <code>cat ~/.bashrc</code></li>
<li>Feche o terminal e abra novamente</li>
<li>Conferir mais uma vez se o Java está instalado</li>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>

<h4>INSTALAÇÃO GIT</h4>
<ol>
<li>Abra o terminal (Ctrl + Alt + t)</li>
<li>Verifique se você tem o GIT instalado: <code>git --version</code></li>
<li>Caso não, instale: <code>sudo apt-get install git-all</code></li>
<li>Verifique se o GIT realmente foi instalado: <code>git --version</code></li>
<li>Configurações iniciais:
<ol>
<li>Configurar o nome de usuário: <code>git config --global user.name "Seu nome"</code></li>
<li>Configurar o endereço de e-mail (o mesmo do GitHub): <code>git config --global user.email seu_email_do_GitHub@email.br</code></li>
<li>Conferir a lista de configurações: <code>git config --list</code></li>
</ol>
</li>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>

<h4>GERAR ACCESS TOKEN</h4>
<ol>
<li>Faça seu login no GitHub</li>
<li><a href="https://github.com/settings/tokens/new">Gere um access token</a>: Your Profile >> Settings >> Developer settings >> Personal access tokens >> Generate new token 
<ol>
<li>Note: Ecolha um nome para o token</li>
<li>Expiration: No expiration</li>
<li>Select scopes: Selecione todos os campos</li>
<li>Generate token</li>
</ol>
</li>
<li>Copie a String referente ao token</li> 
<li>Aalve em um lugar seguro que você consiga consultar posteriormente</li>
<li>Criação e configurações iniciais concluídas!</li>
</ol>

<h4>GERAR SSH KEY</h4>
<ol>
<li>Consulte a <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh">documentação oficial</a></li>
<li>Verifique se <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys">existe alguma SSH key</a> na sua máquina: 
<ol>
<li>No terminal: <code>ls -al ~/.ssh</code></li>
<li>Se sim, para ser válido, o GitHub suporta qualquer um desses nomes de arquivos a seguir:
<ul>
<li>id_rsa.pub</li>
<li>id_ecdsa.pub</li>
<li>id_ed25519.pub</li>
</ul>
</li>
</ol>
<li>Caso não exista, <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent">gere uma SSH key</a>:
<ol>
<li>No terminal: <code>ssh-keygen -t ed25519 -C "seu_email_do_GitHub@example.com"</code></li>
<li>Caso a <em>opção acima não funcione</em>: <code>ssh-keygen -t rsa -b 4096 -C "seu_email_do_GitHub@example.com"</code></li>
<li>Pressione Enter</li>
<li>Pressione Enter</li>
<li>Pressione Enter</li>
</ol>
</li>
<li><a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account">Adicione a nova SSH key na sua conta do GitHub</a>:
<ol>
<li>Abra o arquivo que contém a SSH key publica que você acabou de gerar: <code>cat ~/.ssh/id_ed25519.pub</code></li>
<li>Agora, copie o conteúdo do arquivo id_ed25519.pub que está sendo exibido no terminal</li>
<li><a href="https://github.com/settings/keys">No GitHub</a>: Your Profile >> Settings >> SSH and GPG keys >> New SSH key
<li>Cole o conteúdo da chave pública</li>
</ol>
<li>Teste a conexão SSH: 
<ol>
<li>No terminal: <code>ssh -T git@github.com</code></li>
<li><code>yes</code></li>
</ol>
</li>
<li>Criação e configurações iniciais concluídas!</li>
</ol>

<h4>INSTALAÇÃO INTELLIJ IDEA COMMUNITY</h4>
<li>Show Applications >> Ubuntu Software >> Explore >> Intellij IDEA Community >> Install</li>
<ol>
<li>Entre no <a href="https://www.jetbrains.com/idea/download/#section=linux">site da Jetbrains</a></li>
<li>Escolha a opção Community e faça o Download</li>
<li>Siga com Next</li>
<li>Installation Options:
<ol>
<li>64-bit launcher (caso seu sistema seja 64-bit, caso não, selecione 32-bit)</li>
<li>Add "Open Folder as Project"</li>
<li>.java - .groovy - .kt - .kts</li>
<li>Add lauchers dir to the PATH</li>
<li>Next</li>
</ol>
</li>
<li>Install</li>
<li>Para finalizar a instalação, escolha a opção Reebot later</li>
<li>Configurações Iniciais:</li>
<ol>
<li>Aceite os termos: I confirm that I have... >> Confirm</li>
<li>Data Sharing >> Send Anonymous Statistics</li>
</ol>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>
<hr>

<h2>🍎 macOS</h2>
<h4>INSTALAÇÃO OPENJDK 17.0.4+8 Azul Zulu</h4>
<ol>
<li>Abra o terminal</li>
<li>Verifique se você tem o Java instalado: <code> java --version </code </li>
<li><a href="https://www.azul.com/downloads/?package=jdk">Entre no site oficial da Azul</a></li>
<li>Faça o Download do arquivo <a href="https://cdn.azul.com/zulu/bin/zulu17.36.13-ca-jdk17.0.4-macosx_aarch64.dmg">.dmg</a> (Azul Zulu: 17.0.4+8 x86 64-bit)
<li>Execute o arquivo: Next >> Next >> ... >> Finish</li>
<li>Verifique se o Java realmente foi instalado: <code>java --version</code></li>
<li>Configure a variável em ambiente <code>JAVA_HOME</code>:
<ol>
<li>No Terminal: <code> cd /Library/Java/JavaVirtualMachines</code></li>
<li>Crie o arquivo bash_profile (Vou utilizar o editor nano): <code>nano ~/ .bash_profile</code></li>
<li>Copie o código a seguir e cole no final do arquivo .bash_profile (Observe o caminho do JAVA_HOME): JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-.jdk/Contents/Home</li>
<li>Salve o arquivo .bash_profile</li>
</ol>
<li>Aplicando o caminho da variável: <code>source ~/.bash_profile</code></li>
<li>Confira o caminho da variável <code>JAVA_HOME</code>: <code>echo $JAVA_HOME</code></li>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>

<h4>INSTALAÇÃO GIT</h4>
<ol>
<li>Abra o terminal (Ctrl + Alt + t)</li>
<li>Verifique se você tem o GIT instalado: <code>git --version</code></li>
<li>Caso não, <a href="https://brew.sh/">instale através do Homebrew</a>: 
<ol>
<li><code>/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"</code></li>
<li><code>brew install git</code></li>
</ol>
<li>Verifique se o GIT realmente foi instalado: <code>git --version</code></li>
<li>Configurações iniciais:
<ol>
<li>Configurar o nome de usuário: <code>git config --global user.name "Seu nome"</code></li>
<li>Configurar o endereço de e-mail (o mesmo do GitHub): <code>git config --global user.email seu_email_do_GitHub@email.br</code></li>
<li>Conferir a lista de configurações: <code>git config --list</code></li>
</ol>
</li>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>

<h4>GERAR ACCESS TOKEN</h4>
<ol>
<li>Faça seu login no GitHub</li>
<li><a href="https://github.com/settings/tokens/new">Gere um access token</a>: Your Profile >> Settings >> Developer settings >> Personal access tokens >> Generate new token 
<ol>
<li>Note: Ecolha um nome para o token</li>
<li>Expiration: No expiration</li>
<li>Select scopes: Selecione todos os campos</li>
<li>Generate token</li>
</ol>
</li>
<li>Copie a String referente ao token</li> 
<li>Aalve em um lugar seguro que você consiga consultar posteriormente</li>
<li>Criação e configurações iniciais concluídas!</li>
</ol>

<h4>GERAR SSH KEY</h4>
<ol>
<li>Consulte a <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh">documentação oficial</a></li>
<li>Verifique se <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys">existe alguma SSH key</a> na sua máquina: 
<ol>
<li>No Terminal: <code>ls -al ~/.ssh</code></li>
<li>Se sim, para ser válido, o GitHub suporta qualquer um desses nomes de arquivos a seguir:
<ul>
<li>id_rsa.pub</li>
<li>id_ecdsa.pub</li>
<li>id_ed25519.pub</li>
</ul>
</li>
</ol>
<li>Caso não exista, <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent">gere uma SSH key</a>:
<ol>
<li>No Terminal: <code>ssh-keygen -t ed25519 -C "seu_email_do_GitHub@example.com"</code></li>
<li>Caso a <em>opção acima não funcione</em>: <code>ssh-keygen -t rsa -b 4096 -C "seu_email_do_GitHub@example.com"</code></li>
<li>Pressione Enter</li>
<li>Pressione Enter</li>
<li>Pressione Enter</li>
</ol>
</li>
<li><a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account">Adicione a nova SSH key na sua conta do GitHub</a>:
<ol>
<li>No Terminal: Copie o conteúdo do arquivo id_ed25519.pub: <code>pbcopy < ~/.ssh/id_ed25519.pub</code></li>
<li><a href="https://github.com/settings/keys">No GitHub</a>: Your Profile >> Settings >> SSH and GPG keys >> New SSH key
<li>Cole o conteúdo da chave pública</li>
</ol>
<li>Teste a conexão SSH: 
<ol>
<li>No Terminal: <code>ssh -T git@github.com</code></li>
<li><code>yes</code></li>
</ol>
</li>
<li>Criação e configurações iniciais concluídas!</li>
</ol>

<h4> INSTALAÇÃO INTELLIJ IDEA COMMUNITY </h4>
<ol>
<li>Entre no <a href="https://www.jetbrains.com/idea/download/#section=mac">site da Jetbrains</a></li>
<li>Escolha a opção Community e faça o Download</li>
<li>Siga com Next</li>
<li>Installation Options:
<ol>
<li>64-bit launcher (caso seu sistema seja 64-bit, caso não, selecione 32-bit)</li>
<li>Add "Open Folder as Project"</li>
<li>.java - .groovy - .kt - .kts</li>
<li>Add lauchers dir to the PATH</li>
<li>Next</li>
</ol>
</li>
<li>Install</li>
<li>Para finalizar a instalação, escolha a opção Reebot later</li>
<li>Configurações Iniciais:</li>
<ol>
<li>Aceite os termos: I confirm that I have... >> Confirm</li>
<li>Data Sharing >> Send Anonymous Statistics</li>
</ol>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>
<hr>

<h2> 🤝 Contribuindo </h2>

Este repositório foi criado para fins de estudo, então contribua com ele.
Se te ajudei de alguma forma, ficarei feliz em saber. E caso você conheça alguém que se identidique com o conteúdo, não deixe de compatilhar.

Se possível:

⭐️  Star o projeto

🐛 Encontrar e relatar issues

------------

Disponibilizado com ♥ por [cami-la](https://www.linkedin.com/in/cami-la/ "cami-la").
