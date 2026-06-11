# central-ajuda

Central de ajuda (FAQ) mobile em HTML/CSS/JS puro — sem framework, sem dependência, tudo num arquivo. Busca em tempo real, navegação por categoria, accordion, alertas e checklist por item.

Duas **portas de entrada** pro mesmo tipo de conteúdo, pensadas pra públicos diferentes.

Desenvolvido por **Davi Senise — Técnico de Suporte TI**.

---

## as duas versões

| Arquivo | Porta de entrada | Pensado pra |
|---|---|---|
| [`faq-interno.html`](./faq-interno.html) | Grade de **categorias** → contrato | Equipe interna, que navega por tipo de cliente |
| [`faq-motoboy.html`](./faq-motoboy.html) | **Busca** direta pelo nome do contrato | Entregador em campo, com pressa, que já sabe onde vai |

Mesmo motor, mesma base de dados, interface adaptada ao contexto de uso. O entregador na rua não quer navegar menu — quer digitar e achar. A equipe interna quer ver o panorama por categoria. Resolver o mesmo problema de dois jeitos, conforme quem usa, é a ideia central deste repo.

---

## o que demonstra

- App de página única (SPA) em HTML/CSS/JS puro, sem build, sem framework
- Busca em tempo real filtrando por nome, tipo e tag
- Navegação entre telas e accordion (um item aberto por vez)
- Alertas condicionais e checklist por item (campos opcionais que só renderizam quando existem)
- Design mobile-first, dark, responsivo, com identidade visual própria

---

## como adaptar

Os dados são **fictícios de propósito**. Para usar de verdade, mexa **apenas** no objeto `DADOS` dentro do `<script>` de cada arquivo — o motor não muda.

```javascript
var DADOS = {
  itens: {
    lojaA: {
      nome: "Loja Modelo A", sub: "Varejo", tag: "KM por rota",
      alerta: "Texto do alerta (ou vazio pra não mostrar)",
      checklist: { foto: "...", local: "...", assinatura: "...", nome: "...", obs: "..." },
      topicos: { "Entrega": [ { p: "Pergunta?", r: "Resposta." } ] }
    }
  }
};
```

Troque também o logo (quadrado vermelho no topo), o nome "Empresa Exemplo" e o WhatsApp do rodapé. No `faq-motoboy.html`, troque os links `#` dos vídeos pelos seus.

Campos como `alerta` e `checklist` são opcionais: deixe `alerta` vazio (`""`) ou `checklist` como `null` e o bloco simplesmente não aparece.

---

## nota sobre portfólio

Se adaptar a partir de uma ferramenta interna real, remova **antes** de publicar: telefones, e-mails, links internos (SharePoint/intranet), nomes reais de clientes/contratos, logos de terceiros e qualquer processo confidencial. O motor é o que mostra a habilidade — o dado da empresa fica de fora.

---

## requisitos

Nenhum. Abra o `.html` em qualquer navegador.

---

## autor

**Davi Senise** — Técnico de Suporte TI
[LinkedIn](https://www.linkedin.com/in/davisenise/) · [GitHub](https://github.com/davisenise)
