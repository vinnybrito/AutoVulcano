
# AutoVulcano
API para divulgação de veículos à venda

## Anunciar
Descrição dos endpoints de Anunciar

- `POST` /anunciar: Cadastrar um novo anúncio;
- `GET` /anunciar: Listar todos os anúncios do sistema;
- `GET` /anunciar/{id}: Retornar um veículo especifico;
- `PUT` /anunciar/{id}: Atualizar informações de cadastro;
- `DELETE` /anunciar/{id}: Excluir um anúncio pelo ID;


**Campos da requisição**

| campo | tipo | obrigatório | descrição
|-------|------|:-------------:|---
| id | id | sim | O id precisa ser diferente para cada veículo
| marca | string | sim | Campo para marca do veículo
| modelo | String | sim | Campo para modelo do veículo
| anoModelo | String | sim | Ano do modelo
| anoFabricacao | String | sim | Ano em que o veículo foi fabricado
| versao | String | sim | Variações de um modelo especifico de veículo
| cor | String | sim | Cor do veículo

**Exemplo de JSON**

```js
{
    'id': 1
    'marca': "PEUGEOT",
    'modelo': "308cc",
    'anoModelo': "2015",
    'anoFabricacao': "2015",
    'versao': "Turbo gasolina 2P",
    'cor': "Cinza"
}
```

**Códigos de Resposta**

| código | descrição
|-|-
| 200 | OK
| 201 | Veículo cadastrado com sucesso
| 204 | Ação Executada com sucesso, sem conteudo
| 400 | Os campos enviados são inválidos
| 404 | Página não encontrada
| 405 | Método não permitido
| 500 | Erro interno do servidor


