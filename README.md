# Automação de Processos em Python

## Descrição do Projeto
Este projeto tem como objetivo a automação de processos rotineiros, como o envio de indicadores e relatórios diários para gerentes de lojas e diretoria, utilizando Python. A automação inclui o cálculo dos principais indicadores das lojas e o envio de relatórios personalizados para cada gerente, de forma a permitir um acompanhamento diário e anual do desempenho de suas lojas.

## Bibliotecas Utilizadas
- `Bandas`
- `Pathlib`
- `smtplib`
- `email`
- `mimetypes`
- `unicodedata`

## Objetivo do Projeto
O projeto foi desenvolvido com o intuito de treinar habilidades de programação e automatização de processos em Python, aplicando conhecimentos de manipulação de dados, envio de e-mails e geração de relatórios. A automação substitui um processo que, antes, era realizado manualmente pela equipe de análise de dados de uma grande rede de lojas de roupas.

A equipe, todos os dias pela manhã, precisa calcular os chamados *One Pages* para cada uma das 25 lojas espalhadas pelo Brasil e enviá-los para o respectivo gerente, juntamente com todas as informações usadas no cálculo dos indicadores.

Um *One Page* é um resumo simples e direto, que permite ao gerente da loja verificar rapidamente os principais indicadores e fazer comparações com outras lojas da rede.

## Arquivos e Informações Importantes
- **Emails.xlsx**: contém os nomes, as lojas e os e-mails dos gerentes. Obs: substitua o e-mail dos gerentes por um e-mail próprio para testar o resultado.
- **Vendas.xlsx**: contém as vendas de todas as lojas. Obs: cada gerente recebe apenas o *One Page* e o arquivo em Excel correspondente à sua própria loja. Informações de outras lojas não devem ser enviadas para o gerente que não for da respectiva loja.
- **Lojas.csv**: contém o nome de cada loja.

Ao final da execução do programa, um e-mail também é enviado para a diretoria com dois rankings das lojas anexados: um ranking do dia e outro ranking anual. No corpo do e-mail, destaca-se a melhor e a pior loja do dia, bem como a melhor e a pior loja do ano, com base no faturamento.

As planilhas de cada loja são salvas em uma pasta correspondente, junto com a data da planilha, criando um histórico de backup.

## Indicadores do OnePage
- **Faturamento**
  - Meta Ano: R$ 1.650.000
  - Meta Dia: R$ 1.000
- **Diversidade de Produtos** (quantidade de produtos diferentes vendidos no período)
  - Meta Ano: 120
  - Meta Dia: 4
- **Ticket Médio por Venda**
  - Meta Ano: R$ 500
  - Meta Dia: R$ 500

## Estrutura do Projeto
1. **Leitura dos Arquivos**
   - `Emails.xlsx` para obter informações dos gerentes e da diretoria.
   - `Vendas.xlsx` para calcular os indicadores e separar as vendas por loja.
   - `Lojas.csv` para identificar o nome das lojas e associá-las ao gerente.

2. **Cálculo dos Indicadores**
   - Os indicadores de faturamento, diversidade de produtos e ticket médio são calculados tanto para o dia quanto para o ano.
   - São definidos critérios para metas e o status dos indicadores é exibido com cores diferentes (verde para meta atingida e vermelho para não atingida).

3. **Geração dos Relatórios**
   - Relatórios diários são gerados para cada loja e salvos na pasta de backup, seguindo a estrutura `{dia}_{mês}_{loja}.xlsx`.

4. **Envio dos E-mails**
   - Cada gerente recebe um e-mail com o *One Page* e o relatório de vendas de sua loja.
   - A diretoria recebe um e-mail com os rankings das lojas e a indicação da melhor e pior loja do dia e do ano.

## Como Executar o Projeto
1. Certifique-se de que você tem as bibliotecas necessárias instaladas.
2. Baixe ou clone este repositório.
3. Adicione os arquivos de entrada (`Emails.xlsx`, `Vendas.xlsx` e `Lojas.csv`) à pasta do projeto.
4. Execute o script principal (`automacao_processos.py`) para iniciar o processo de automação.

## Considerações
Este projeto foi desenvolvido como um exercício de automação de processos, visando melhorar a eficiência na comunicação entre a equipe de análise de dados e os gerentes de loja. Ele também serve como um exemplo prático de como a automação pode ser usada para substituir tarefas repetitivas e garantir precisão e consistência nos resultados.

Sinta-se à vontade para contribuir, sugerir melhorias ou utilizar este projeto como base para outros casos de uso.

---

### Contato
Qualquer dúvida, estou à disposição.

Att.,  
Márcio Luiz
