# Cuckoo Log Reader

Ferramenta em Python para leitura e extração de informações de arquivos JSON gerados pelo **Cuckoo Sandbox**.  
O objetivo é facilitar a análise de logs de comportamento, rede e outras features, permitindo filtros avançados via **linha de comando** ou **menu interativo**.

---

## 🎯 Objetivo
Este artefato foi desenvolvido como parte da disciplina de **Artefato de Softwares em Cibersegurança**.  
Ele aborda o problema de **processamento de logs** em ambientes de análise dinâmica de malware, oferecendo uma solução simples, reprodutível e containerizada.

---

## ⚙️ Funcionalidades
- [Leitura de JSON](ca://s?q=Leitura_de_JSON_do_Cuckoo) reportado pelo Cuckoo.
- [Menu interativo](ca://s?q=Menu_interativo_para_extracao) para explorar dados.
- [Filtros avançados](ca://s?q=Filtros_avancados_para_extracao) para extrair subchaves específicas (ex: processos dentro de `behavior`).
- [Execução em Docker](ca://s?q=Rodar_aplicacao_em_Docker) para garantir reprodutibilidade.

---

## 🚀 Estrutura do projeto

cuckoo-log-reader/
│── main.py          # Script principal
│── requirements.txt # Dependências
│── Dockerfile       # Container
│── README.md        # Documentação


## 🚀 Como usar
```bash
docker build -t cuckoo-log-reader .
docker run -it --rm -v $(pwd):/app cuckoo-log-reader
```

## 🚀 Exemplo de uso

Digite o caminho do arquivo JSON: report.json

===== MENU =====
1. Listar todas as chaves disponíveis
2. Extrair uma chave específica
3. Extrair uma subchave dentro de uma chave
4. Sair

### 1. Clonar o repositório
```bash
git clone https://github.com/seuusuario/cuckoo-log-reader.git
cd cuckoo-log-reader

