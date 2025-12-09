# Sensoriamento

> Todo o trabalho de Sensoriamento foi desenvolvido nesse repositório

[Link para repositório](https://github.com/BrunoBReis/Sensoriamento-PR-Gama-2025.2)

Este módulo concentra todos os códigos, testes e experimentos relacionados ao **subsistema de Sensoriamento** do projeto.  
Ele funciona como um ambiente de desenvolvimento isolado para validação de técnicas de processamento de imagens que futuramente poderão ser integradas ao sistema completo do satélite.

---

## Organização do diretório `sensoriamento/`

A estrutura do diretório foi pensada para separar claramente **código-fonte**, **imagens de teste** e **scripts de apoio ao desenvolvimento**:

- `sensoriamento/src/`  
  Contém os arquivos-fonte em **C++** responsáveis pelo processamento de imagens.

- `sensoriamento/images/`  
  Conjunto de imagens utilizadas nos testes do processamento (nuvens, rios, regiões agrícolas, cenários artificiais, etc.).

- `sensoriamento/scripts/`  
  Scripts auxiliares para facilitar o fluxo de desenvolvimento:
  - `build.sh` → compila o projeto
  - `clean.sh` → limpa os arquivos de build
  - `lsp.sh` → integração com servidor de linguagem (LSP)

- `sensoriamento/CMakeLists.txt`  
  Arquivo responsável por configurar o processo de compilação do módulo usando **CMake** e **OpenCV**.

Essa organização permite manter o módulo de Sensoriamento **independente dos demais subsistemas** (TT&C e OBC), facilitando testes, manutenção e evolução.


## Como compilar o módulo de Sensoriamento

### 1. Pré-requisitos

Antes de compilar, é necessário ter instalado no sistema:

- Compilador C++ (`g++` ou equivalente)
- `cmake` (versão 3.10 ou superior)
- `make`
- Bibliotecas de desenvolvimento do **OpenCV**

Em distribuições Linux baseadas em Debian/Ubuntu, por exemplo:

```bash
sudo apt install g++ cmake make libopencv-dev
```

### 2. Compilando com o script de build

A partir da raiz do repositório:

```bash
cd sensoriamento/scripts
./build.sh
```

Esse processo irá:

1. Acessar automaticamente a pasta `sensoriamento/`
2. Criar a pasta `build/` caso não exista
3. Executar o `cmake` usando o `CMakeLists.txt` local
4. Compilar todos os arquivos da pasta `src/`

Ao final, a compilação será concluída com sucesso e os binários ficarão disponíveis na pasta `build/`.


## Como executar os programas de Sensoriamento

Após a compilação, entre na pasta de build:

```bash
cd sensoriamento/build
```

E execute o binário desejado:

```bash
./main
```

> O nome do executável corresponde ao nome do arquivo `.cpp` presente em `src/`.


## Limpando os arquivos de build

Caso seja necessário recompilar tudo do zero:

```bash
cd sensoriamento/scripts
./clean.sh
```

Isso remove completamente a pasta `build/` e os arquivos temporários de compilação.


## Integração com LSP (opcional)

Para quem utiliza editores com suporte a servidor de linguagem (como Neovim, VS Code ou CLion), é possível executar:

```bash
cd sensoriamento/scripts
./lsp.sh
```

Esse script cria um link simbólico para o arquivo `compile_commands.json`, permitindo que o editor reconheça corretamente as configurações do projeto em C++.

## Autoria

Projeto desenvolvido por:

- **[Bruno Bragança](https://github.com/BrunoBReis)**
- **[Pedro Victor](https://github.com/pedroslrn)**

No contexto do **Projeto Trainee 2025 – Gama Cube Design**.
