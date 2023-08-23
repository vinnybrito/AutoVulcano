
# AutoVulcano
A API AutoVulcano é uma interface RESTful para o cadastro e divulgação de anúncios de veículos à venda. A documentação abrange endpoints, formatos de entrada/saída e códigos de retorno, garantindo uma integração eficiente.

## Anunciar
### Listar todos os anúncios

- Método: `GET`
- Endpoint: /anunciar
- Descrição: Retorna a lista de todos os anúncios do sistema.

**Exemplo JSON**

```js
{
    'id': 1
    'marca': "PEUGEOT",
    'modelo': "308cc",
    'anoModelo': "2015",
    'anoFabricacao': "2015",
    'versao': "Turbo gasolina 2P",
    'cor': "Cinza"
    // ... outros anúncios
}
```

### Retornar um veículo especifico;

- Método: `GET`
- Endpoint: /anunciar/{id}
- Descrição: Retorna um anúncio específico com base no seu ID.

**Exemplo JSON**

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

### Cadastrar veículo

- Método: `POST`
- Endpoint: /anunciar
- Descrição: Cadastrar um veículo para realizar publicação do anúncio;

```js
{
    'marca': "PEUGEOT",
    'modelo': "308cc",
    'anoModelo': "2015",
    'anoFabricacao': "2015",
    'versao': "Turbo gasolina 2P",
    'cor': "Cinza"
}
```

### Editar informações de cadastro

Editar anúncio por ID

- Método: PUT
- Endpoint: /anunciar/{id}
- Descrição: Edita uma Anúncio existente com base no seu ID.

Formato de entrada (JSON):

```js
{
    'marca': "PEUGEOT",
    'modelo': "308cc",
    'anoModelo': "2015",
    'anoFabricacao': "2015",
    'versao': "Turbo gasolina 2P",
    'cor': "Cinza"
}
```

## Deletar anúncio por ID

- Método: DELETE
- Endpoint: /anunciar/{id}
- Descrição: Deleta um anúncio do sistema com base no seu ID.


---


**Campos da requisição**

| campo | tipo | obrigatório | descrição
|-------|------|:-------------:|---
| id | id | sim | O id precisa ser diferente para cada veículo
| marca | String | sim | Campo para marca do veículo
| modelo | String | sim | Campo para modelo do veículo
| anoModelo | String | sim | Ano do modelo
| anoFabricacao | String | sim | Ano em que o veículo foi fabricado
| versao | String | sim | Variações de um modelo especifico de veículo
| cor | String | sim | Cor do veículo



**Descrição dos endpoints de Anunciar**

- `POST` /anunciar: Cadastrar um novo anúncio;
- `GET` /anunciar: Listar todos os anúncios do sistema;
- `GET` /anunciar/{id}: Retornar um veículo especifico;
- `PUT` /anunciar/{id}: Atualizar informações de cadastro;
- `DELETE` /anunciar/{id}: Excluir um anúncio pelo ID;



**Códigos de Retorno**

| Código | Descrição
|-|-
| 200 | Requisição bem-sucedida
| 201 | Veículo cadastrado com sucesso
| 204 | A requisição foi bem-sucedida, mas não há conteúdo para retornar.
| 400 | Os campos enviados são inválidos
| 404 | Página não encontrada
| 405 | Método não permitido
| 500 | Erro interno do servidor
