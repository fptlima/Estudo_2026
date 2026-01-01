🌐 1. Como a Internet funciona por baixo dos panos
Independente da tecnologia que você usar (React, Node.js, etc.), tudo começa com a comunicação entre duas partes: o Cliente e o Servidor.

Modelo Cliente-Servidor: O cliente (seu navegador ou aplicativo) abre uma conexão e envia um pedido (Request). O servidor processa esse pedido e devolve uma resposta (Response).

DNS (O catálogo da rede): Quando você digita google.com, o navegador faz uma busca de DNS para transformar esse nome em um endereço IP (números que identificam o servidor na rede).

A "Porta" de Entrada: Por padrão, a comunicação HTTP acontece na porta 80.

📄 2. O Protocolo HTTP (Hypertext Transfer Protocol)
O HTTP é a linguagem que permite a transferência de documentos hipermídia, como o HTML.

Stateless (Sem Estado): O HTTP é nativamente um protocolo "sem memória". Isso significa que o servidor não guarda dados entre uma requisição e outra; cada conexão é tratada como se fosse a primeira.

Camada de Aplicação: Ele vive no topo da pilha de protocolos (TCP/IP), o que significa que nós, desenvolvedores, lidamos diretamente com ele sem precisar nos preocupar com como os cabos ou placas de rede funcionam.

⚡ 3. Verbos (Métodos) HTTP
Os verbos indicam a ação que você quer realizar em um recurso. Os mais importantes para o seu dia a dia serão:

GET: Solicita dados de um recurso (ex: carregar uma página).

POST: Envia dados para o servidor para criar algo novo ou mudar um estado (ex: formulário de login ou cadastro).

PUT: Substitui todos os dados de um recurso específico.

PATCH: Aplica modificações parciais em um recurso.

DELETE: Remove um recurso específico.

Diferença Crucial: No método GET, os parâmetros vão visíveis diretamente na URL (ex: google.com/search?q=linux). No POST, os dados vão "escondidos" dentro do corpo (body) da requisição.

🚦 4. Códigos de Status (As respostas do servidor)
Sempre que o servidor responde, ele envia um código numérico agrupado em cinco classes:

1xx (Informação): Requisição recebida e processando.

2xx (Sucesso): Tudo certo! O código 200 OK é o mais comum.

3xx (Redirecionamento): O recurso mudou de lugar. Ex: 301 Moved Permanently.

4xx (Erro do Cliente): Você fez algo errado. Ex: 404 Not Found (página não existe).

5xx (Erro do Servidor): O problema é no site/servidor. Ex: 500 Internal Server Error (erro de código ou banco fora do ar).

🍪 5. Cookies e Sessões
Se o HTTP não tem memória, como o site sabe que você está logado? Através de Cookies.

O servidor envia um cabeçalho Set-Cookie. O navegador armazena essa informação e a envia de volta em todos os próximos pedidos.

Isso permite criar Sessões, onde um ID de cookie no seu PC corresponde a um espaço de memória no servidor com seus dados (como o carrinho de compras).

🔒 6. Segurança: HTTPS
Para informações sensíveis (senhas, cartões), o HTTP sozinho é perigoso porque os dados viajam abertos na rede. O HTTPS resolve isso usando criptografia, garantindo que ninguém no meio do caminho consiga ler o que está sendo enviado.

📝 Exercício Prático para você:
Abra o seu Git Bash e tente "ver" o HTTP acontecendo no seu computador atual (o LOJA-PC) usando o comando curl (que funciona como um cliente HTTP simples):

Digite: curl -I https://www.google.com

Observe o código de status (provavelmente 200 OK) e os cabeçalhos que aparecem.