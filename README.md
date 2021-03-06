# DAppHeroesNFT
 Projeto DApp que permite interação com Tokens padrão ERC20 e ERC721, baseado em blockchain.

## Project Goals
- Cria um DApp
- Apilicação web com Blazor WebAssembly
- Smart Contracts baseado em rede Ethereum
    - Smart Contracts desenvolvido na linguagem de programação "solidity";
    - Conjunto de Smart Contracts que permite clamar tokens e mintar NFT por meio da aplicação web.

## Dependencies
- .Net 6.0 
- Ganache
- MetaMask

## Frontend
- Blazor WebAssembly "dotnet new blazorwasm -o DAppHeroesNFT" para criar a estrutura de front-end.
    - Blazor Wasm permite Interoperabilidade C#/JavaScript.
- Personalização com Bootstrap.

## Blockchain
- DApp criado em ambiente ethereum usando ferramentas e bibliotecas como:
    - Web3js;
    - Ethers.js;
    - Ganache;
    - Remix IDE

## Smart contracts
- Remix IDE para desenvolvimento e teste dos Smart Contracts.
    - IDE Online acessada pelo site 
- Para auxiliar na segurança dos Smart Contracts, utilizamos bibliotecas da OpenZeppelin.
    - OpenZeppelin fornece produtos de segurança para construir, automatizar e operar aplicativos descentralizados. 

## Contract 1 - Token.sol
- Token ERC20.
- Token "Heroes of Peace - HPT".
- Smart Contract responsável pelo controle do Token.
 

## Contract 2 - TokenClaim.sol
- Smart Contract responsável para clamar 10 tokens HPT por vez. Será permitido clamar 10 tokens HPT somente se o balanço do usuário(endereço) estiver com zero token HPT no momento do claim.

## Contract 3 - HeroNFT.sol
- Token ERC721.
- Token "Heroes of Peace NFT". Smart Contract responsável por emitir e armazenar os NFTs. Para mintar um NFT o emissor tem que está habilitado para mintar segundo regra implementada no Smart Contract.
- Os NFT mintado possuem 4 tipos de Classe: A,B,C e D. A chances para cada uma das classes são:
    - Classe A: 10% Bithex;
    - Classe B: 15% Ethenia;
    - Classe C: 25% Cardimande;
    - Classe D: 50% Linkah.

## Contract 4 - HeroNFTGenerate.sol
- Smart Contract responsável por verificar se o usuário(endereço) está hábil para mintar um NFT, e estando hábil faz uma chamada para o contrato HeroNFT.sol dando continuidade no processo.
- Para está hábil a mintar um NFT, o usuário precisa ter 10 Tokens HPT em seu balanço e também precisa ter dado a permissão para o endereço do Smart Contract utilizar esses 10 Tokens HPT.

## References
- OpenZeppe: https://openzeppelin.com/
- Referência de códigos solidity: https://github.com/OpenZeppelin
- IDE Remix: https://remix.ethereum.org/

## Project result
<p align="center">
    <img src="assets/to_readme/videoDApp.gif" />
</p>
