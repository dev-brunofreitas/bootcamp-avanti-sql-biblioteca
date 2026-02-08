# bootcamp-avanti-sql-biblioteca
Projeto de banco de dados relacional para gestão de biblioteca desenvolvido no Bootcamp Avanti.

Este repositório contém a implementação física de um banco de dados relacional para a gestão de uma biblioteca. O projeto faz parte dos desafios práticos de SQL utilizando metodologias ágeis.

🛠️ Tecnologias e Ferramentas
* Banco de Dados: PostgreSQL
* Gerenciador: DBeaver
* Gestão de Projeto: Jira (Metodologia SCRUM)

📑 Progresso do Projeto (Sprints)

✅ Task 4: Implementação Física e DML (Concluída)
* Criação das tabelas livros, membros e emprestimos.
* Configuração de Primary Keys e Foreign Keys para garantir a integridade dos dados.
* Scripts de automação com DROP TABLE IF EXISTS para limpeza de ambiente.
* Povoamento inicial do banco com dados de teste (Livros, Membros e registros de Empréstimos).

 📸 Evidências
(Dica: Aqui você pode colocar o print que você tirou do DBeaver mostrando o grid preenchido com os dados)
<img width="2868" height="1800" alt="image" src="https://github.com/user-attachments/assets/4bbed8b9-d017-4375-8a74-529045d43916" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/7b8bb368-e03c-4857-b3eb-10d4bb913459" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/7bff2f82-0e69-47c5-8ff0-780b31f8aadc" />
<img width="2868" height="1800" alt="image" src="https://github.com/user-attachments/assets/d3489773-3760-469b-a231-94cde8a101fd" />
<img width="1434" height="908" alt="image" src="https://github.com/user-attachments/assets/d16a5518-59e3-4c33-a6b2-b2b5afaf37a3" />



Como rodar o projeto

Certifique-se de ter o PostgreSQL instalado.

Abra o script script_biblioteca_task4.sql no seu editor SQL (recomendo DBeaver).

Execute o script completo para criar a estrutura e inserir os dados.

# 📚 Bootcamp Avanti - Sistema de Gestão de Biblioteca

Projeto de banco de dados relacional para gestão de biblioteca, desenvolvido como parte dos desafios do Bootcamp Avanti.

## 🛠️ Tecnologias Utilizadas
* **Banco de Dados:** PostgreSQL
* **Ferramenta de Gestão:** DBeaver
* **Controle de Versão:** Git & GitHub

---

## 🚀 Task 5 - Consultas e Inteligência de Dados
Nesta etapa, o foco foi extrair informações estratégicas do banco de dados utilizando consultas SQL avançadas.

### Cenários Resolvidos:

#### A) Livros emprestados a membros de São Paulo
* **Técnica:** Utilização de `DISTINCT` e múltiplos `JOINs`.
* **Lógica:** O `DISTINCT` foi aplicado para que, caso existam vários empréstimos do mesmo livro para pessoas de SP, o título apareça apenas uma vez, evitando duplicidade no relatório.

#### B) Número de empréstimos por membro
* **Técnica:** `LEFT JOIN`, `COUNT` e `GROUP BY`.
* **Lógica:** Usei `LEFT JOIN` para garantir que membros com zero empréstimos também apareçam na lista. O atributo `AS` foi utilizado para renomear a coluna calculada e tornar o resultado mais legível.

#### C) Livros não devolvidos (Pendências)
* **Técnica:** Filtro `IS NULL`.
* **Lógica:** Identificação de registros onde a `data_devolucao` está vazia. Foi utilizado `IS NULL` em vez de `= NULL`, respeitando a sintaxe correta do SQL para valores nulos.

#### D) Livros publicados antes do ano 2000
Esta foi a consulta mais complexa do projeto devido à diversidade dos dados (ex: "500 a.C.").
* **Regex (`~ '^[0-9]+$'`):** Validou se o dado era puramente numérico antes da conversão.
* **CAST:** Converteu o `VARCHAR` em `INTEGER` para realizar a comparação matemática.
* **OR & LIKE:** Garantiu que livros históricos (a.C.) fossem incluídos na contagem final junto aos anos numéricos.

#### E) Livros nunca emprestados
* **Técnica:** Subquery com `NOT IN`.
* **Lógica:** Identifica livros cujos ISBNs não constam na tabela de empréstimos.

#### F) Livro mais emprestado
* **Técnica:** `ORDER BY DESC` e `LIMIT 1`.
* **Lógica:** Organiza o ranking de empréstimos do maior para o menor e isola o primeiro colocado.

---

## 📈 Conclusão do Aprendizado
O projeto permitiu dominar conceitos fundamentais de SQL, desde a criação da estrutura (DDL) até o tratamento de tipos de dados complexos e lógica de filtragem avançada.


### 📸 Evidências da Task 5

<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/5fffa435-3c0c-4c31-8323-fc07da4322e3" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/0f3d4086-a6a6-4ab7-931e-a580bab53667" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/4db1b835-af4d-4e2e-832a-de72d5cc75ac" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/381db34d-3a61-4994-ae9b-150aa7e9a17f" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/bc831ff1-f937-462d-8596-65fe6edd4060" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/c9698c64-68c1-40b7-b5b7-09435f358726" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/48dd0a9e-9a78-4510-8d15-c790099a984e" />
<img width="1168" height="768" alt="image" src="https://github.com/user-attachments/assets/10e04549-bac5-44da-b1f2-812f21b6c22f" />







