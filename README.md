# Brazilian Exchange Helper

O **Brazilian Exchange Helper** é uma biblioteca .NET que fornece funcionalidades para lidar com taxas de câmbio brasileiras. Ele oferece uma maneira fácil de obter dados completos de taxas de câmbio para uma determinada data e moeda, além de suporte a cache para melhorar o desempenho da aplicação.

## Instalação

Você pode baixar a biblioteca **Brazilian Exchange Helper** diretamente do GitHub. Para isso, siga estas etapas:

1. **Clone o repositório**:

   Clone este repositório para o seu ambiente de desenvolvimento local usando Git:

   ```bash
   git clone https://github.com/seu-usuario/brazilian-exchange-helper.git
   ```

2. **Adicione a biblioteca ao seu projeto**:

   Adicione a biblioteca **Brazilian Exchange Helper** ao seu projeto como um projeto de referência ou copie os arquivos de código-fonte diretamente para a sua solução.

3. **Configure o serviço de taxas de câmbio**:

   Configure o serviço de taxas de câmbio em sua aplicação, geralmente em um arquivo de configuração ou no código de inicialização. Certifique-se de registrar o serviço na injeção de dependência, fornecendo uma implementação de `IMemoryCache`.

4. **Obtenha os dados de taxas de câmbio**:

   Use o serviço de taxas de câmbio para obter os dados completos de taxas de câmbio para uma determinada data e moeda. O método `GetFullExchangeData` retorna um objeto `ExchangeRateModel` com as informações necessárias.

```csharp
// Exemplo de uso do serviço de taxas de câmbio
var exchangeService = serviceProvider.GetService<IExchangeRateService>();
var exchangeData = await exchangeService.GetFullExchangeData("2024-05-23", "USD");
Console.WriteLine($"Taxa de compra: {exchangeData.ExchangePurchase}");
Console.WriteLine($"Taxa de venda: {exchangeData.ExchangeSale}");
```

5. **Opções avançadas**:

   A biblioteca oferece suporte a cache para melhorar o desempenho. Os dados de taxas de câmbio são armazenados em cache por um período configurável para evitar chamadas excessivas à API.

## Contribuindo

Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões de melhorias, fique à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).
