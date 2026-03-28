<!-- LOGOTIPO DO PROJETO -->
<div style="display: flex; justify-content: center;">
   <a href="https://github.com/edendenis/python">
     <img src="figures/gold_edf_technology_logo_transparent_background_and_gold_name.png" alt="Logo" width="160" height="160">
   </a>
</div>

<h3 align="center">Configurar/instalar/usar o `Python 3.8` no `Linux Ubuntu`</h3>

<!-- <div style="display: flex; justify-content: center;">
  <a href="https://zenodo.org/doi/10.5281/zenodo.10668919">
    <img src="https://zenodo.org/badge/758237447.svg" alt="DOI">
  </a>
</div> -->

<p align="center">
 Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `Google Chrome` no `Linux Ubuntu`.
 <br />
 <a href="https://github.com/edendenis/python"><strong>Explore os documentos »</strong></a>
 <br />
 <br />
 <a href="https://github.com/edendenis/python">Ver demonstração</a>
 ·
 <a href="https://github.com/edendenis/python">Relatar bug</a>
 ·
 <a href="https://github.com/edendenis/python">Solicitar recurso</a>
</p>




# Configurar/instalar/usar o `Python 3.8` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `Python 3.8` no `Linux Ubuntu`.

## _Abstract_

_In this document are contained the main commands and settings to set up/install the `Python 3.8` on `Linux Ubuntu`._




### Construído com

Esta seção deve listar todas as principais estruturas/bibliotecas usadas para inicializar seu projeto. Deixe quaisquer complementos/plugins para a seção de agradecimentos. Aqui estão alguns exemplos.

* [![Python 3.8](https://img.shields.io/badge/Python%203.8-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)

* [![Anaconda](https://img.shields.io/badge/Anaconda-44A833?style=flat-square&logo=anaconda&logoColor=white)](https://www.anaconda.com/)

* [![Jupyter Collaboration](https://img.shields.io/badge/Jupyter%20Collaboration-F37626?style=flat-square&logo=Jupyter&logoColor=white)](https://jupyter.org/)

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>




<!-- COMEÇANDO -->
### Começando

Este é um exemplo de como você pode dar instruções sobre como configurar seu projeto localmente.
Para obter uma cópia local instalada e funcionando, siga estas etapas simples de exemplo.



### Pré-requisitos

Este é um exemplo de como listar os itens necessários para usar o _software_ e como instalá-los.

* Python 3.8

* Anaconda 24.1.0

* Git

* IDE para executar o arquivo `.ipynb` (PyCharm, Spyder, VS Code etc.)

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>




## Descrição [2]

### `Python`

O `Python` é uma linguagem de programação de alto nível, interpretada e multiparadigma, conhecida por sua simplicidade e legibilidade. Criada por Guido van Rossum e lançada em 1991, `Python` oferece uma sintaxe clara e concisa, tornando-a ideal para iniciantes e experientes. Sua ampla biblioteca padrão e vasta comunidade de desenvolvedores facilitam a criação de uma variedade de aplicativos, desde scripts simples até aplicativos web complexos, aprendizado de máquina e ciência de dados. `Python` é valorizado por sua portabilidade, interoperabilidade e escalabilidade, sendo uma escolha popular em muitas áreas da computação e além.

## 1. Como configurar/instalar/usar o `Python` no `Linux Ubuntu` [1]

Para configurar/instalar/usar o `Python` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```

    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```

    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```

3. Baixe a versão desejada do python em: <https://www.python.org/>

Instalar o `Python` no `Linux Ubuntu` via `Terminal Emulator` é um processo relativamente simples. O `Linux Ubuntu` já vem com o `Python` pré-instalado, mas você pode querer instalar uma versão específica ou atualizar a existente. Aqui estão os passos para instalar o `Python` ou atualizar para uma versão específica:

1. **Instalar `Python 3.x`**: Se você quiser instalar uma versão específica do `Python 3.x`, você pode especificar o número da versão. Por exemplo, para instalar o `Python 3.8`:

    ```bash
    sudo apt install python3.8 -y
    ```

2. **Verificar a Instalação**: Para verificar se o `Python` foi instalado corretamente e qual versão está instalada, execute:

    ```bash
    python3 --version
    ```

### 1.1 Adicionar o `Python` ao `$PATH` do `Linux Ubuntu`

Para garantir que o comando python no `Terminal Emulator` aponte para o `Python 3` em vez de uma versão anterior (ou de não apontar para nada), você pode criar um _link_ simbólico que faz com que o comando `python` execute `python3`. Aqui está como você pode fazer isso:

1. **Verificar a versão do `Python 3`**: Primeiro, verifique onde o `python3` está localizado:

    ```bash
    whereis python3
    ```

    Isso retornará o caminho completo para o executável `python3`. Anote esse caminho, pois você precisará dele mais tarde. Normalmente, o caminho é algo como:
    
    ```bash
    /usr/bin/python3
    ```

2. **Criar um _Link_ Simbólico**: Para criar um _link_ simbólico para que o comando `python` aponte para `python3`, use o seguinte comando:

    ```bash
    sudo ln -s /usr/bin/python3 /usr/bin/python
    ```

    Aqui, `/usr/bin/python3` deve ser substituído pelo caminho que você obteve na etapa anterior, se for diferente.

3. **Verificar a Alteração**: Verifique se o _link_ simbólico foi criado corretamente e se `python` agora aponta para o `Python 3`:

    ```bash
    python --version
    ```

    Isso deve mostrar a versão do `Python 3`, indicando que o _link_ simbólico foi criado corretamente.

4. **Verificar o _Link_ Simbólico**: Verifique se o _link_ simbólico foi criado corretamente:

    ```bash
    ls -l /usr/bin/python
    ```

    Isso deve mostrar algo como:
    
    ```bash
    lrwxrwxrwx 1 root root 16 Aug  6 12:34 /usr/bin/python -> /usr/bin/python3
    ```

    Se não estiver apontando para `/usr/bin/python3`, então o _link_ simbólico não foi criado corretamente.

5. **Reinicie o `Terminal Emulator`**: Às vezes, o erminal pode não refletir mudanças imediatamente. Tente fechar e reabrir o `Terminal Emulator` ou usar o comando `hash -r `para limpar o _cache_ do caminho dos comandos.

6. **Verificar a Versão**: Certifique-se de que o comando `python` está chamando a versão correta do `Python`:

    ```bash
    python --version
    ```



## 1.2 Instalar o `pip` para o `Python 3.x`

O `pip` pode não estar instalado automaticamente com o `Python`. Você pode instalar o `pip` usando o `apt` (o gerenciador de pacotes do `Linux Ubuntu`) ou o _script_ de instalação `get-pip.py`. Primeiro, vamos tentar instalar o `pip` usando `apt`.

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```

    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```

    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```

3. **Instalar o `pip`**: Tente instalar o `pip` para `Python 3` usando o seguinte comando:

    ```bash
    sudo apt install python3-pip -y
    ```

4. **Verificar a Instalação do `pip`**: Depois de instalar o `pip`, verifique se está funcionando:

    ```bash
    pip3 --version
    ```

    Isso deve mostrar a versão do `pip` instalada.



## 2. Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `Python` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```bash
    NÂO há.
    ```




<!-- LICENÇA -->
## Licença

Distribuído sob a licença MIT. Consulte `LICENSE.txt` para obter mais informações.

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>



<!-- ROTEIRO -->
## Roteiro

- [x] Adicionar registro de alterações

- [x] Adicionar links de volta ao topo

- [x] Adicionar modelos adicionais com exemplos

- [x] Suporte multilíngue

     - [ ] Espanhol

     - [ ] Inglês

     - [ ] Português
     
     - [x] Português brasileiro 

Consulte os [problemas abertos](https://github.com/edendenis/google_chrome/issues) para obter uma lista completa dos recursos propostos (e problemas conhecidos).

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>




<!-- CONTRIBUIÇÔES -->
## Contribuições

As contribuições são o que tornam a comunidade de código aberto um lugar incrível para aprender, inspirar e criar. Qualquer contribuição que você fizer será **muito apreciada**.

Se você tiver uma sugestão que possa melhorar isso, bifurque o repositório e crie uma solicitação `pull`. Você também pode simplesmente abrir um problema com a tag “aprimoramento”.
Não se esqueça de dar uma estrela ao projeto! Obrigado novamente!

1. Bifurque o projeto

2. Crie sua ramificação de recursos (`git checkout -b feature/AmazingFeature`)

3. Confirme suas alterações (`git commit -m 'Add some AmazingFeature'`)

4. Envie para a filial (`git push origin feature/AmazingFeature`)

5. Abra uma solicitação `pull`

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>




<!-- ACKNOWLEDGMENTS -->
## Agradecimentos

* [Best README Template](https://github.com/othneildrew/Best-README-Template?tab=readme-ov-file)

* [Choose an Open Source License](https://choosealicense.com)

* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)

* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)

* [Malven's Grid Cheatsheet](https://grid.malven.co/)

* [Img Shields](https://shields.io)

* [GitHub Pages](https://pages.github.com)

* [Font Awesome](https://fontawesome.com)

* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>




## Referências

[1] OPENAI. **Instalar o python no ubuntu.** Disponível em: <https://chat.openai.com/c/0ce53031-41c5-4185-93d7-0156e1d2cb2a> (texto adaptado). Acessado em: 13/03/2024 13:47.

[2] OPENAI. **Vs code: editor popular.** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 13/03/2024 13:48.
