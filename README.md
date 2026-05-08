# Análise de Dados

Repositório oficial de apoio à disciplina **Análise de Dados**, ofertada no curso de **Ciência de Dados para Negócios da Universidade Federal da Paraíba (UFPB)**.

Este projeto reúne bases de dados, notebooks, scripts e materiais de apoio para atividades práticas envolvendo análise exploratória, preparação de dados, visualização, modelagem estatística e comunicação de resultados com Python.

---

## Professor responsável

**Aléssio Almeida**  
Universidade Federal da Paraíba — UFPB  
Laboratório de Estudos em Modelagem Aplicada — LEMA  
E-mail: alessio@lema.ufpb.br

---

## Objetivo do repositório

O repositório foi criado para apoiar o desenvolvimento de competências práticas em análise de dados, com foco em:

- organização e leitura de bases de dados;
- limpeza, transformação e preparação de dados;
- análise exploratória de dados;
- construção de indicadores;
- visualização e comunicação de evidências;
- uso de Python, pandas, NumPy, matplotlib, plotly e bibliotecas relacionadas;
- desenvolvimento de scripts reprodutíveis;
- boas práticas de organização de projetos analíticos.

A disciplina adota uma abordagem aplicada, orientada a problemas reais e à produção de análises úteis para tomada de decisão.

---

# Preparação do ambiente

Esta seção apresenta os softwares necessários para acompanhar as aulas, executar os notebooks e desenvolver as atividades práticas da disciplina.

---

## 1. Requisitos de software

### Softwares obrigatórios

Instale os seguintes programas antes das primeiras atividades práticas:

- **Python 3**  
  https://www.python.org/downloads/

- **Visual Studio Code — VS Code**  
  https://code.visualstudio.com/download

- **Git**  
  https://git-scm.com/downloads

- **PIP — gerenciador de pacotes do Python**  
  https://pip.pypa.io/en/stable/installation/

- **Jupyter Notebook ou JupyterLab**  
  Será instalado pelo `requirements.txt`, mas também pode ser instalado manualmente com:

```bash
pip install jupyter
```

### Softwares recomendados

- **Antigravity — Google**  
  https://antigravity.google/

- **GitHub Desktop**  
  https://desktop.github.com/

- **Anaconda ou Miniconda**  
  https://docs.conda.io/en/latest/miniconda.html

### Softwares extras

Esses softwares não são obrigatórios para a execução dos códigos da disciplina, mas podem ser úteis para produção de textos acadêmicos, relatórios e referências bibliográficas:

- **Mendeley**  
  https://www.mendeley.com/download-reference-manager/windows

- **Overleaf**  
  https://www.overleaf.com

- **MiKTeX**  
  https://miktex.org/download

- **TeXstudio**  
  https://www.texstudio.org/

---

## 2. Verificação da instalação

Após instalar os programas obrigatórios, abra o terminal e verifique se os comandos abaixo funcionam.

### Verificar Python

```bash
python --version
```

ou, em alguns sistemas:

```bash
python3 --version
```

### Verificar PIP

```bash
pip --version
```

ou:

```bash
pip3 --version
```

### Verificar Git

```bash
git --version
```

Se algum desses comandos não funcionar, o programa pode não ter sido instalado corretamente ou pode não estar configurado no `PATH` do sistema operacional.

---

## 3. Clonando o repositório

Depois de instalar o Git, clone este repositório para o seu computador.

```bash
git clone https://github.com/seu-usuario/analise-de-dados.git
cd analise-de-dados
```

Substitua `https://github.com/seu-usuario/analise-de-dados.git` pelo endereço real do repositório da disciplina.

---

## 4. Abrindo o projeto no VS Code

Com o terminal aberto dentro da pasta do projeto, execute:

```bash
code .
```

Esse comando abre o projeto no Visual Studio Code.

Caso o comando `code .` não funcione, abra o VS Code manualmente e selecione:

```text
File > Open Folder
```

Em seguida, escolha a pasta do projeto.

---

# Principais bibliotecas

Crie um arquivo chamado `requirements.txt` na raiz do projeto com as bibliotecas necessárias para execução dos notebooks e scripts da disciplina.

Uma sugestão inicial é:

```txt
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
plotly>=5.15.0
scipy>=1.10.0
statsmodels>=0.14.0
scikit-learn>=1.3.0
jupyter>=1.0.0
notebook>=7.0.0
jupyterlab>=4.0.0
openpyxl>=3.1.0
pyarrow>=14.0.0
requests>=2.31.0
python-dotenv>=1.0.0
ipykernel>=6.0.0
```

Essas bibliotecas cobrem as principais tarefas da disciplina:

- leitura e manipulação de dados;
- análise exploratória;
- visualização;
- modelagem estatística;
- machine learning;
- leitura de arquivos Excel, CSV e Parquet;
- execução de notebooks.

---

## 5. Criando o ambiente virtual

Recomenda-se criar um ambiente virtual na raiz do projeto.

O ambiente virtual isola as bibliotecas instaladas para este projeto, evitando conflitos com outros projetos Python existentes no computador.

---

## 5.1 Windows — Git Bash

```bash
python -m venv venv
source venv/Scripts/activate
```

Após ativar o ambiente virtual, atualize o `pip`:

```bash
python -m pip install --upgrade pip
```

Instale as bibliotecas:

```bash
pip install -r requirements.txt
```

---

## 5.2 Windows — PowerShell

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

Depois, atualize o `pip`:

```powershell
python -m pip install --upgrade pip
```

Instale as bibliotecas:

```powershell
pip install -r requirements.txt
```

Caso o PowerShell bloqueie a ativação do ambiente virtual, execute:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Depois tente novamente:

```powershell
.\venv\Scripts\Activate.ps1
```

---

## 5.3 macOS ou Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

Após ativar o ambiente virtual, atualize o `pip`:

```bash
python -m pip install --upgrade pip
```

Instale as bibliotecas:

```bash
pip install -r requirements.txt
```

---

## 6. Verificando se o ambiente está ativo

Quando o ambiente virtual estiver ativo, o terminal normalmente exibirá o prefixo `(venv)` antes do caminho da pasta.

Exemplo:

```bash
(venv) usuario@computador analise-de-dados %
```

Também é possível verificar qual Python está sendo usado.

### Windows

```bash
where python
```

### macOS ou Linux

```bash
which python
```

O caminho retornado deve apontar para a pasta `venv` do projeto.

---

## 7. Abrindo o Jupyter Notebook

Com o ambiente virtual ativo, execute:

```bash
jupyter notebook
```

Ou, se preferir usar JupyterLab:

```bash
jupyter lab
```

O navegador será aberto com a interface do Jupyter.

---

## 8. Selecionando o ambiente no VS Code

No VS Code, abra um notebook `.ipynb` e selecione o kernel Python do ambiente virtual.

O caminho geralmente será semelhante a:

```text
./venv/bin/python
```

no macOS/Linux, ou:

```text
.\venv\Scripts\python.exe
```

no Windows.

Se o kernel do ambiente virtual não aparecer automaticamente, instale o pacote `ipykernel`:

```bash
pip install ipykernel
```

Depois registre o kernel:

```bash
python -m ipykernel install --user --name analise-dados --display-name "Python - Análise de Dados"
```

---

## 9. Desativando o ambiente virtual

Ao final do uso, o ambiente virtual pode ser desativado com:

```bash
deactivate
```

---

# Atualização do arquivo requirements.txt

Durante o desenvolvimento das atividades, novas bibliotecas podem ser instaladas individualmente:

```bash
pip install nome-da-biblioteca
```

Ao final, é possível congelar as versões instaladas com:

```bash
pip freeze > requirements.txt
```

Esse procedimento registra todas as bibliotecas instaladas no ambiente virtual.

No entanto, para projetos didáticos, recomenda-se manter o `requirements.txt` enxuto, incluindo apenas as bibliotecas realmente utilizadas nos notebooks e scripts.

---

# Estrutura sugerida do repositório

```text
analise-de-dados/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── raw/              # Dados brutos, sem alterações manuais
│   ├── processed/        # Dados tratados e prontos para análise
│   └── external/         # Dicionários, códigos, metadados e bases auxiliares
│
├── notebooks/
│   ├── 01_introducao_python.ipynb
│   ├── 02_pandas.ipynb
│   ├── 03_analise_exploratoria.ipynb
│   └── ...
│
├── scripts/
│   ├── 01_extract.py
│   ├── 02_transform.py
│   ├── 03_analysis.py
│   └── 04_visualization.py
│
├── outputs/
│   ├── figures/          # Gráficos gerados
│   ├── tables/           # Tabelas exportadas
│   └── reports/          # Relatórios e produtos finais
│
└── docs/
    └── materiais_apoio.md
```

---

# Organização das bases de dados

As bases de dados devem ser armazenadas na pasta `data/`, respeitando a seguinte lógica.

## `data/raw/`

Dados originais, exatamente como foram obtidos.

Não devem ser modificados manualmente.

Exemplo:

```text
data/raw/municipios.csv
data/raw/microdados_enem.csv
data/raw/indicadores_educacionais.xlsx
```

## `data/processed/`

Dados tratados, padronizados, filtrados ou agregados.

Exemplo:

```text
data/processed/indicadores_municipais.csv
data/processed/base_modelagem.parquet
```

## `data/external/`

Bases auxiliares externas, como dicionários, malhas territoriais, tabelas de códigos, classificações ou metadados.

Exemplo:

```text
data/external/codigos_ibge.csv
data/external/dicionario_variaveis.xlsx
```

---

# Controle de versionamento

O uso de Git é recomendado para acompanhar a evolução dos códigos, notebooks e materiais da disciplina.

Fluxo básico:

```bash
git status
git add .
git commit -m "Atualiza notebooks da aula 01"
git push
```

Boas práticas:

- fazer commits pequenos e descritivos;
- não versionar ambiente virtual;
- não versionar bases sigilosas;
- evitar versionar arquivos muito grandes;
- manter o `README.md` atualizado;
- usar branches para alterações maiores.

---

# Arquivo .gitignore recomendado

Crie um arquivo chamado `.gitignore` na raiz do projeto com o seguinte conteúdo:

```gitignore
# Sistema operacional
.DS_Store
Thumbs.db

# Ambientes virtuais
venv/
.venv/
env/
.env/
*venv/
*.venv/

# Python
__pycache__/
*.py[cod]
*.pyo
*.pyd

# Jupyter
.ipynb_checkpoints/

# Arquivos temporários
*.tmp
*.log
~$*.xls*
~$*.xlsx
~$*.docx

# Configurações locais e variáveis de ambiente
.env
.env.local

# Testes e cache
.pytest_cache/
.mypy_cache/
.coverage

# Dados privados ou restritos
data/raw/private/
data/raw/restricted/
data/sensitive/

# Bancos locais
*.db
*.sqlite
*.sqlite3

# Outputs temporários
outputs/temp/
outputs/cache/
```

---

# Política de dados

Este repositório pode conter bases públicas, bases simuladas ou bases didáticas.

Antes de adicionar qualquer base de dados, verifique:

- se a base é pública;
- se não contém informações pessoais sensíveis;
- se há autorização para compartilhamento;
- se a fonte dos dados está documentada;
- se há dicionário de variáveis ou metadados.

Dados restritos, identificados ou sensíveis não devem ser disponibilizados publicamente neste repositório.

---

# Produtos esperados dos estudantes

Ao longo da disciplina, os estudantes poderão desenvolver:

- notebooks de análise;
- scripts de tratamento de dados;
- tabelas descritivas;
- gráficos analíticos;
- painéis exploratórios;
- relatórios técnicos;
- projetos finais baseados em dados reais.

Um produto analítico mínimo deve conter:

1. pergunta de análise;
2. descrição da base de dados;
3. tratamento e preparação dos dados;
4. análise exploratória;
5. visualizações adequadas;
6. interpretação dos resultados;
7. limitações da análise;
8. conclusão orientada à decisão.

---

# Contato

Dúvidas, sugestões ou correções podem ser encaminhadas para:

**Aléssio Almeida**  
E-mail: alessio@lema.ufpb.br  
Laboratório de Estudos em Modelagem Aplicada — LEMA  
Universidade Federal da Paraíba — UFPB
