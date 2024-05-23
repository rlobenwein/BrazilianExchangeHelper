# Brazilian Exchange Helper

O **Brazilian Exchange Helper** � uma biblioteca .NET que fornece funcionalidades para lidar com taxas de c�mbio brasileiras. Ele oferece uma maneira f�cil de obter dados completos de taxas de c�mbio para uma determinada data e moeda, al�m de suporte a cache para melhorar o desempenho da aplica��o.

## Instala��o

Voc� pode baixar a biblioteca **Brazilian Exchange Helper** diretamente do GitHub. Para isso, siga estas etapas:

1. **Clone o reposit�rio**:

   Clone este reposit�rio para o seu ambiente de desenvolvimento local usando Git:

   ```bash
   git clone https://github.com/seu-usuario/brazilian-exchange-helper.git
   ```

2. **Adicione a biblioteca ao seu projeto**:

   Adicione a biblioteca **Brazilian Exchange Helper** ao seu projeto como um projeto de refer�ncia ou copie os arquivos de c�digo-fonte diretamente para a sua solu��o.

3. **Configure o servi�o de taxas de c�mbio**:

   Configure o servi�o de taxas de c�mbio em sua aplica��o, geralmente em um arquivo de configura��o ou no c�digo de inicializa��o. Certifique-se de registrar o servi�o na inje��o de depend�ncia, fornecendo uma implementa��o de `IMemoryCache`.

4. **Obtenha os dados de taxas de c�mbio**:

   Use o servi�o de taxas de c�mbio para obter os dados completos de taxas de c�mbio para uma determinada data e moeda. O m�todo `GetFullExchangeData` retorna um objeto `ExchangeRateModel` com as informa��es necess�rias.

```csharp
// Exemplo de uso do servi�o de taxas de c�mbio
var exchangeService = serviceProvider.GetService<IExchangeRateService>();
var exchangeData = await exchangeService.GetFullExchangeData("2024-05-23", "USD");
Console.WriteLine($"Taxa de compra: {exchangeData.ExchangePurchase}");
Console.WriteLine($"Taxa de venda: {exchangeData.ExchangeSale}");
```

5. **Op��es avan�adas**:

   A biblioteca oferece suporte a cache para melhorar o desempenho. Os dados de taxas de c�mbio s�o armazenados em cache por um per�odo configur�vel para evitar chamadas excessivas � API.

## Contribuindo

Contribui��es s�o bem-vindas! Se voc� encontrar algum problema ou tiver sugest�es de melhorias, fique � vontade para abrir uma issue ou enviar um pull request.

## Licen�a

Este projeto est� licenciado sob a [Licen�a MIT](LICENSE).
