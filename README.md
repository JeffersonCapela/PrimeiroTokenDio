# DIOJToken - ERC-20 Token

Este projeto implementa um token padrão **ERC-20** chamado **DIOJToken**, desenvolvido durante o curso da **Digital Innovation One (DIO)** em parceria com a **Binance**. O token pode ser usado como base para a criação de criptomoedas seguindo o padrão Ethereum.

## Descrição do Token

**DIOJToken** é um token criado para aprendizado, com uma implementação simplificada de um contrato ERC-20 utilizando o Solidity. O token permite transferências entre contas, aprovações e transferências delegadas, além de uma função para queimar tokens.

### Detalhes do Token:
- **Nome:** DIOJ Token
- **Símbolo:** DIOJ
- **Decimais:** 18
- **Total Supply Inicial:** Definido no momento do deploy

## Funcionalidades

O contrato implementa as seguintes funcionalidades do padrão ERC-20:

- **Total Supply:** Retorna a quantidade total de tokens em circulação.
- **Balance Of:** Verifica o saldo de um endereço específico.
- **Transfer:** Transfere tokens diretamente de uma conta para outra.
- **Approve:** Aprova uma quantidade de tokens para ser gasta por um terceiro.
- **Allowance:** Verifica quanto um terceiro está autorizado a gastar de uma conta.
- **Transfer From:** Permite que uma conta transfira tokens de outra, com base na aprovação.
- **Burn:** Permite que o criador do token queime uma quantidade de tokens, reduzindo o total em circulação.

## Como implantar o contrato

### Pré-requisitos

- **Node.js** e **npm** instalados
- **Hardhat** configurado para o ambiente de desenvolvimento Ethereum
- Conta no **MetaMask** ou outro provedor de carteira Ethereum
- **Remix IDE** ou **Hardhat** para fazer o deploy

### Deploy via Hardhat

1. Instale o Hardhat:
   ```bash
   npm install --save-dev hardhat
   
2.Crie um novo projeto Hardhat e inicialize:


npx hardhat

3.Adicione o contrato ao projeto na pasta contracts.
4.Compile o contrato:

bash
Copiar código
npx hardhat compile
Execute o script de deploy:

javascript

async function main() {
  const DIOJToken = await ethers.getContractFactory("DIOJToken");
  const diojToken = await DIOJToken.deploy("DIOJ Token", "DIOJ", ethers.utils.parseEther("10"));
  await diojToken.deployed();
  console.log("DIOJ Token deployed to:", diojToken.address);
}

main();
5.Execute o deploy:

bash

npx hardhat run scripts/deploy.js --network rinkeby
Deploy via Remix IDE
Acesse o Remix IDE.
Crie um novo arquivo e cole o código do contrato.
Compile o contrato na versão ^0.8.0 do Solidity.
Conecte o MetaMask e faça o deploy passando os parâmetros: DIOJ Token, DIOJ e o valor inicial da oferta de tokens.
Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

6.Licença
Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

perl

### Como utilizar:
- Crie um arquivo chamado `README.md` no diretório raiz do seu projeto e copie o conteúdo acima para ele.
- Esse arquivo `README.md` servirá como uma documentação básica do projeto no GitHub, explicando o que o token faz e como foi desenvolvido.







