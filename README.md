# MSCardápioDigital — Modelo para GitHub e Vercel

## Publicar e testar no celular

1. Extraia este ZIP no computador.
2. Crie um repositório no GitHub para o modelo.
3. Envie o conteúdo desta pasta: `index.html`, `imagens`, `vercel.json` e este README. Não envie apenas o ZIP.
4. O `index.html` deve estar na raiz do repositório, ao lado da pasta `imagens`.
5. Na Vercel, crie um projeto e importe esse repositório.
6. Em Framework Preset, selecione **Other**. Deixe Build Command vazio. O `vercel.json` já configura a saída na raiz (`.`), sem build.
7. Publique com Deploy e abra o endereço gerado no navegador do celular.

Não há instalação, dependências de build, backend ou banco de dados. Os estilos e as funções continuam dentro do HTML. As imagens agora são arquivos separados.

## Personalizar para cada estabelecimento

Copie o projeto para um novo repositório e edite o bloco `<script id="configuracao">` no começo de `index.html`:

- Nome, marca, logo, cores dos temas e horários.
- Produtos, categorias, descrições, valores e adicionais.
- Caminhos das fotos na pasta `imagens`.
- `logoImage`: por exemplo, `imagens/logo.png`. Adicione o arquivo correspondente.
- `hero.image`: foto do banner.
- `delivery.enabled`: `false` para desativar Delivery.
- Taxa fixa, bairros/regiões atendidos, frete grátis e retirada.
- `payments.methods`: somente as formas de pagamento aceitas.
- Chave Pix, titular, cidade e banco do estabelecimento.
- WhatsApp do estabelecimento.

Cada cliente terá uma publicação independente, na qual você poderá conectar o subdomínio desejado.

## Dados atuais do teste

O projeto contém o cardápio fictício Brasa Burger, taxa fixa de R$ 5,00, retirada grátis, WhatsApp e chave Pix reais fornecidos para teste. Revise e substitua esses dados ao replicar para outra loja. O banco do Pix está vazio, aguardando cadastro.

## Funcionamento

Consulta do cardápio ou Delivery, carrinho em memória, adicionais, taxas, CEP com alternativa manual, seleção de pagamento e troco, QR Code Pix/Copia e Cola e resumo para WhatsApp. O QR Code gera uma instrução de pagamento; o banco do pagador mostra os dados reais da chave. O estabelecimento confere o recebimento. O comprovante é anexado manualmente pelo cliente na conversa.

Somente a preferência de tema fica salva no navegador. Carrinho e formulário se perdem ao recarregar. Fontes web, consulta de CEP, WhatsApp e pagamento exigem internet. A geração do QR é local, com a biblioteca incorporada.

## Conferir no celular

- Temas claro e escuro e logo no cabeçalho/rodapé.
- Busca, categorias, abertura de fotos e fechamento dos pop-ups.
- Adicionais, quantidades, carrinho e taxas de entrega/retirada.
- Preenchimento por CEP e preenchimento manual.
- Pix, dinheiro com troco, crédito e débito.
- QR Code, cópia do Pix e abertura do WhatsApp.

## Créditos

Desenvolvido por MSCardápioDigital.
QR Code Generator for JavaScript, Kazuhiko Arase, versão 1.4.4, licença MIT (aviso preservado no HTML).
Fotos de exemplo obtidas do Unsplash; substitua pelas imagens do estabelecimento.

Documentação: https://vercel.com/docs/builds/configure-a-build
