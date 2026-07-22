# ADYMIDIAS — publicação do site e verificação do negócio na Meta

Guilherme Ady Teixeira Leal · CNPJ 58.727.888/0001-49

---

## Ordem de execução

A sequência importa. Publicar o site antes de resolver o domínio e o e-mail
desperdiça o principal sinal de credibilidade.

### 1. Domínio (faça primeiro)

- Registrar `adymidias.com.br` no **Registro.br**.
- **Titular do domínio = CNPJ 58.727.888/0001-49.** Não registrar em CPF.
  A Meta consulta WHOIS; domínio no CNPJ da empresa é o sinal mais forte que existe.
- Custo aproximado: R$ 40/ano.

### 2. E-mail corporativo

- Criar `contato@adymidias.com.br` (Zoho Mail tem plano gratuito para 1 domínio;
  Google Workspace custa mais e funciona igual para esse fim).
- Trocar o e-mail administrativo do Business Manager para esse endereço.
- O Gmail pessoal continua funcionando, mas não serve como e-mail da empresa
  numa análise de verificação.

### 3. Hospedagem

Qualquer um serve, todos com HTTPS automático:

- **Netlify** — arraste a pasta em `app.netlify.com/drop`, depois aponte o domínio.
- **Cloudflare Pages** — gratuito, rápido, bom painel de DNS.
- **Vercel** — igualmente simples.

Depois de publicar, confirme que `https://www.adymidias.com.br` abre com cadeado
e que as 4 páginas carregam.

### 4. Ajustes obrigatórios antes de subir

Faça um localizar-e-substituir em todos os arquivos:

| Substituir | Por |
|---|---|
| `contato@adymidias.com.br` | seu e-mail real, se o domínio for outro |
| `www.adymidias.com.br` | seu domínio real |
| `(31) 9944-4626` | o telefone com o mesmo formato do cartão CNPJ |
| `+553199444626` | o mesmo número, em formato internacional |

**Atenção ao telefone:** o cartão CNPJ mostra `(31) 9944-4626` — 8 dígitos.
Se for celular, falta o 9. O número no site precisa ser **idêntico** ao do
cadastro e precisa atender de verdade. Se estiver errado no cadastro, corrija
na Receita antes.

### 5. Formulário de contato

O arquivo `contato.html` tem, no final, a variável:

```js
var ENDPOINT_FORMULARIO = "";
```

Vazio, o formulário abre o programa de e-mail do visitante com a mensagem pronta
(funciona, mas é menos elegante). Para receber por e-mail de verdade:

1. Crie uma conta gratuita no Formspree.
2. Cole o endpoint entre as aspas.

Um formulário que funciona é sinal de site vivo. Vale os 5 minutos.

---

## Os três pontos que podem travar a verificação

### a) "ADYMIDIAS" não consta no seu CNPJ

O campo **Título do Estabelecimento (Nome de Fantasia)** está com asteriscos no
comprovante. A Meta compara o nome do site com o documento enviado.

O site já resolve isso mostrando razão social + CNPJ no cabeçalho, na ficha
cadastral do topo, no rodapé e nos dois documentos legais — a marca ADYMIDIAS
aparece sempre acompanhada do titular.

Mesmo assim, o ideal é **incluir o nome fantasia no cadastro** pelo portal
Redesim/JUCEMG. É uma alteração cadastral simples e barata, e elimina de vez
a pergunta "o que é ADYMIDIAS?".

### b) Congruência do CNAE

Tudo no site está escrito dentro de **73.19-0-02 — Promoção de vendas**:
serviço prestado para terceiros, gestão de campanhas, mensuração, relatório.
Não invente serviço que não caiba nesse CNAE (desenvolvimento de software,
venda de produto próprio, consultoria financeira). Incongruência entre o que o
site diz e o que o CNPJ registra é exatamente o que derruba a análise.

### c) Nada inventado

O site não tem cliente fictício, número de faturamento, depoimento nem selo.
Isso é proposital. Se quiser adicionar prova social depois, use só o que for
verdadeiro e comprovável — case falso é risco maior do que ausência de case.

---

## Depois de publicar

1. Deixe o site no ar **por alguns dias** antes de abrir a verificação.
   Site registrado ontem tem peso menor.
2. Cadastre no **Google Search Console** e envie o `sitemap.xml`. Site indexado
   no Google é verificável por qualquer analista.
3. No **Meta Business Suite → Central de Segurança → Verificação do negócio**:
   - Nome legal: `GUILHERME ADY TEIXEIRA LEAL` (exatamente como no cartão)
   - CNPJ: `58.727.888/0001-49`
   - Endereço: exatamente como no cartão, incluindo "Casa B"
   - Site: `https://www.adymidias.com.br`
   - E-mail: `contato@adymidias.com.br`
   - Documento: o Comprovante de Inscrição e Situação Cadastral (o mais recente)
4. Se pedirem confirmação por e-mail ou telefone, use os mesmos do site.

**Regra única:** o que está no cartão CNPJ, no site e no formulário da Meta
precisa bater caractere por caractere. Divergência de endereço ou de nome é a
causa mais comum de reprovação.

---

## Observação sobre o enquadramento

Um dos arquivos enviados se chama `mei.pdf`, mas o comprovante mostra
**Natureza Jurídica 213-5 — Empresário Individual, porte ME** — que não é a
mesma coisa que MEI. Vale confirmar com seu contador em qual regime a empresa
está de fato, porque isso afeta emissão de nota fiscal e obrigações mensais.
Não muda nada no site, mas muda no dia a dia.
