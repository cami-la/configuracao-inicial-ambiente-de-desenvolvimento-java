<h2>🐧 LINUX</H2>
<h4>Instalação OpenJDK 17</h4>
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
</ol>
