<h2>🐧 LINUX</H2>
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
<li>Vamos configurar a variável em ambiente <code>JAVA_HOME</code>:</li>
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

<h4>GERAR SSH key</h4>
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
</ol>
</li>
<li><a href="https://github.com/settings/keys">No GitHub</a>: Your Profile >> Settings >> SSH and GPG keys >> New SSH key
<li>Cole o conteúdo da chave pública</li>
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

<h4>INSTALAÇÃO VISUAL STUDIO CODE</h4>
<li>Show Applications >> Ubuntu Software >> Explore >> Visual Studio Code >> Install</li>

<ol>
<li>Entre no site oficial do Visual Studio Code</li>
<li>Faça o <strong><a href="https://code.visualstudio.com/">DOWNLOAD</a></strong> do arquivo com a extensão .deb</li>
<li>Escolha a opção Open With: Software install (default)</li>
<li>Pesquise o VS code nas suas aplicações</li>
<li><a href="https://code.visualstudio.com/docs/languages/java">Configuração para desenvolvimento Java:</a>
<ol>
<li>Abrir o Vs code</li>
<li>Abrir o menu de extensões: (Ctrl + Shift + X)</li>
<li>Colar o comando: <code>vscode:extension/vscjava.vscode-java-pack</code></li>
</ol>
</li>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>

<h4>INSTALAÇÃO ECLIPSE IDE</h4>
<li>Show Applications >> Ubuntu Software >> Explore >> Eclipse >> Install</li>
<ol>
<li><a href="https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2022-06/R/eclipse-inst-jre-linux64.tar.gz">Entre no site oficial do Eclipse Foundation e faça o Download</a></li>
<li>Descompacte a pasta</li>
<li>Procure o arquivo "eclipse-inst" e execute</li>
<li>Escolha segunda a opção: Eclipse IDE for Enterprise Java and Web Developers</li>
<li>Clique no folder da primeira opção e selecione o JDK instalado na sua máquina</li>
<li>Mantenha as opções "create start menu entry" e "create desktop shortcut"</li>
<li>Install</li>
<li>Accept now</li>
<li>Launch</li>
<li>Pesquise o Eclipse IDE nas suas aplicações</li>
<li>Instalação e configurações iniciais concluídas!</li>
</ol>
