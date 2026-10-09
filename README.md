Fatores associados à proficiência em Língua Portuguesa no Ensino Médio público de Mato Grosso (SAEB 2023)

Este repositório reúne o código e os dados usados na dissertação de mestrado

Fatores associados à proficiência em Língua Portuguesa no Ensino Médio público de Mato Grosso: uma análise por mineração de dados educacionais com dados do SAEB 2023
Amauri Bambolim — Programa de Pós-Graduação em Educação e Novas Tecnologias, Uninter, 2026.
O objetivo é permitir que qualquer pessoa confira e reproduza todas as tabelas e figuras da pesquisa, e que outras secretarias, escolas e pesquisadores possam adaptar os procedimentos a outros recortes.

## O que há aqui

|Arquivo|Conteúdo|
|-|-|
|`consulta\_saeb2023\_mt.sql`|Consulta usada para extrair os microdados do SAEB 2023 na Base dos Dados (Google BigQuery)|
|`saeb2023\_mt\_bruta\_completa.csv`|Resultado dessa consulta: 24.464 registros de estudantes|
|`01\_base\_analitica.ipynb`|Da base bruta à base analítica: exclusões, recodificação e tratamento das respostas ausentes|
|`02\_descritivas\_e\_testes.ipynb`|Estatísticas descritivas, testes de diferença entre grupos e tamanhos de efeito|
|`03\_regressao.ipynb`|Regressão linear com erros-padrão agrupados por escola e análises de sensibilidade|
|`04\_comparacao\_metodos.ipynb`|RReliefF, Random Forest e comparação das medidas de relevância dos atributos|
|`04b\_comparacao\_categorias.ipynb`|A mesma comparação, com as categorias dos atributos nominais separadas|
|`05\_resiliencia.ipynb`|Resiliência acadêmica com o INSE do INEP|
|`06\_validade\_q23b.ipynb`|Verificação da validade da resposta ao item Q23b (estilos de resposta)|
|`07\_analises\_complementares.ipynb`|Níveis de proficiência, língua falada em casa e outras análises complementares|
|`requirements.txt`|Bibliotecas Python usadas|

Os notebooks estão salvos com os resultados já calculados. Para ver as tabelas e figuras, basta abrir o notebook aqui mesmo no GitHub.

## Os dados

Os dados são os microdados públicos do SAEB 2023, divulgados pelo INEP e disponibilizados pela [Base dos Dados](https://basedosdados.org) (tabela `basedosdados.br\_inep\_saeb.aluno\_em\_34ano`). Os códigos de escola, turma e estudante são mascarados pelo próprio INEP, e não há nenhuma informação que permita identificar pessoas.

Recorte: Mato Grosso, escolas públicas, prova de Língua Portuguesa, estudantes presentes, 3ª série do Ensino Médio e 4ª série do Ensino Médio integrado.

## Como reproduzir no Google Colab

1. No seu Google Drive, crie uma pasta chamada `dissertacao` em "Meu Drive".
2. Baixe deste repositório o arquivo `saeb2023\_mt\_bruta\_completa.csv` e coloque-o nessa pasta.
3. Abra os notebooks no Google Colab (em [colab.research.google.com](https://colab.research.google.com), menu **Arquivo → Fazer upload de notebook**).
4. Execute os notebooks **na ordem**, de 01 a 07. O notebook 01 gera a base analítica que todos os outros usam. Em cada um, use **Ambiente de execução → Executar tudo** e autorize o acesso ao Drive quando o Colab pedir.
5. As tabelas (planilhas `.xlsx`) e as figuras (`.png`) são salvas na pasta `dissertacao`.

O notebook 04 leva de 8 a 15 minutos para rodar. Os demais levam poucos minutos.

Para usar outra pasta, altere a linha `PASTA = '/content/drive/MyDrive/dissertacao/'` no início de cada notebook.

## Reprodutibilidade

* Todas as etapas com sorteio usam a mesma semente (2025).
* Cada notebook imprime, no início, as versões das bibliotecas usadas.
* Pequenas diferenças na terceira casa decimal podem ocorrer com versões diferentes das bibliotecas, sem alterar as conclusões.

## Como citar

\[Referência da dissertação, no formato ABNT]

## Licença

O código está sob a licença MIT (arquivo `LICENSE`): pode ser usado, adaptado e redistribuído, desde que a autoria seja citada. Os dados pertencem ao INEP e seguem as condições de uso dos microdados públicos.

