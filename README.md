
# Consulta do titular de domínio utilizando RDAP do Registro.BR

Esse script em Python foi criado originalmente para consultar o CPF/CNPJ do titular dos domínios que estão listados na planilha e comparar com outra planilha validando se os documentos são compatíveis entre elas.
É possível alterar a consulta para qualquer parâmetro desejado que esteja presente na saída do https://rdap.registro.br/domain/








## Instalação

- Crie um ambiente virtual em python para o projeto
- Instale as bibliotecas que serão necessárias:

```bash
  pip install openpyxl requests tqdm
```






## Observações
- Verifique se preencheu corretamente o nome e caminho das planilhas que serão usadas. 
- O script utiliza Session() method para reusar conexões TCP que já foram abertas.
- O tempo de duração do script varia conforme a quantidade de domínios que possui em sua planilha, uma vez que há uma pausa de 7 minutos a cada 29 consultas. Isso foi criado pois o RDAP do Registro.BR bloqueia o IP quando ocorre mais de 30 consultas em 5 minutos. 
