<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="Logotipo da bestimage.ai"></a></p>

# Awesome Wan 3.0 Prompts — Guia em português do Brasil

**148 propostas de direção de vídeo em 14 categorias, adaptadas e mantidas pela equipe da [bestimage.ai](https://bestimage.ai/).** Defina um acontecimento claro, atribua funções às entradas e planeje câmera, som e continuidade.

[Guia em inglês](README.md) · [Os 15 idiomas](locales/README.md) · [Índice completo](prompts/README.md) · [Contribuir](CONTRIBUTING.md)

![Ilustração conceitual de uma pessoa do arquivo abrindo um mapa estelar em um observatório ao amanhecer](assets/wan-3-prompt-collection-hero.png)

*Ilustração estática criada com a ferramenta integrada de geração de imagens, não um vídeo gerado pelo Wan 3.0. Consulte as [instruções das imagens e sua procedência](assets/README.md).*

## Conteúdo e primeiros passos

**148 propostas de direção de vídeo em 14 categorias**. As seis primeiras categorias têm instruções de direção em chinês; as outras oito, em inglês. Os 15 idiomas abrangem guias de entrada e um exemplo comparativo comum, **não traduções completas das 148 propostas**. As traduções e o exemplo comparativo não entram na contagem como propostas adicionais.

1. Escolha uma proposta no [índice completo](prompts/README.md).
2. Ajuste as variáveis e prepare todas as entradas indicadas. As referências descrevem funções; seus arquivos não são fornecidos neste repositório.
3. Selecione a modalidade e configure duração, proporção, resolução e som na interface. O texto sozinho não configura uma requisição de API.
4. Faça um teste pequeno e confira ação, geometria, identidade, ritmo e som de acordo com o objetivo de revisão da proposta.

## Fórmula de oito camadas

```text
[Saída] duração + proporção + linguagem visual
[Sujeito] características de identidade reutilizáveis + detalhes imutáveis
[Ambiente] horário + local + clima + profundidade espacial
[Ação] gatilho → movimento contínuo → resultado visível
[Câmera] enquadramento + ângulo + um percurso + quadro final
[Aparência] luz + paleta + materiais + tratamento do movimento
[Som] ambiente + efeitos + música + diálogo
[Restrições] elementos a preservar + falhas mais prováveis
```

Use um idioma principal para a descrição visual e indique separadamente o idioma e as falas exatas do diálogo. Recursos e configurações dependem do produto, da região e da plataforma.

## Exemplo comparativo completo

**Modalidade:** texto para vídeo · **Configurações:** 10 segundos, 16:9, som ativado · **Entradas:** nenhuma

```text
Crie um plano documental de 10 segundos em formato 16:9 em uma tranquila biblioteca comunitária de ferramentas. Uma pessoa adulta voluntária, de cabelo curto e cacheado, usando avental cor de mostarda e camisa azul-marinho com as mangas arregaçadas, conserta um pequeno ventilador de mesa vermelho que está fora da tomada. De 0 a 3 segundos, a pessoa coloca a grade de proteção removida ao lado do ventilador parado. De 3 a 7 segundos, tira a poeira de uma das pás com um pano macio enquanto a câmera desliza lentamente para a direita na altura do tampo da mesa. De 7 a 10 segundos, deixa o pano e alinha a grade com a carcaça, sem conectar o ventilador à tomada nem ligá-lo. A luz da janela revela o metal desgastado e a textura do algodão. Som: atrito do pano, um clique suave da grade e ambiente tranquilo da sala; sem fala nem música. Preserve a mesma pessoa, o mesmo ventilador, suas três pás, a carcaça vermelha e o cabo fora da tomada. Sem pás girando, ferramentas adicionais, etiquetas legíveis, legendas ou cortes.
```

**Variáveis:** cor do avental, cor do ventilador e iluminação da sala. **Revisão:** o ventilador permanece fora da tomada e parado; a quantidade de pás e o contato das mãos continuam coerentes. Este é um conceito criativo, não uma instrução de reparo elétrico.

## API Wan 3.0 na bestimage.ai

Estas páginas em inglês apresentam a interface de teste e os exemplos públicos de requisições.

| Modalidade | Preparação e finalidade |
|---|---|
| [Texto para vídeo](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) | Descrição completa de uma cena com causa, ação intermediária e resultado visível. |
| [Imagem para vídeo](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) | Imagem inicial **e imagem final** na modalidade documentada; explicar a transição e preservar geometria e composição. |
| [Referências para vídeo](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) | Referências opcionais de identidade, objeto, espaço, movimento ou som; atribuir uma função a cada recurso. |
| [Edição de vídeo](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) | Vídeo de origem e uma alteração delimitada; preservar atuação, duração, câmera e áreas não modificadas. |

O [guia de API e controle de custos](guides/bestimage-wan-3-api.md) explica requisições, consultas de andamento e planejamento de testes. **O servidor de API da bestimage.ai é `https://api.flaq.ai`.** Use uma chave de API emitida pela sua conta bestimage.ai.

Consulte a página do modelo e sua conta antes de gastar créditos. As modalidades correspondem à documentação da bestimage.ai; isso não significa que todos os produtos Wan tenham os mesmos controles.

## GPT Image 2 para preparar referências visuais

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) gera imagens estáticas; [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) edita imagens e combina referências visuais. Use-os para preparar fichas de personagens, referências de produtos ou composições iniciais e finais aprovadas antes de uma tarefa de vídeo.

São **modelos de imagem separados**, não interfaces de vídeo do Wan. Exporte e confira as imagens antes de fornecê-las à modalidade Wan adequada. O repositório não automatiza essa transferência nem afirma que as ilustrações conceituais foram geradas por essas APIs. Consulte o [fluxo de preparação das referências](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow).

## Navegação, guias e contribuições

O [índice das 148 propostas](prompts/README.md) abrange narrativa cinematográfica, produtos, conteúdo de usuários, alimentação e viagens, esportes, animação, música, serviços, ciência, arquitetura, produção, comércio, diálogos, natureza e indústria.

Os guias de [escrita de instruções](guides/prompting-guide.md), [capacidades e limites](guides/model-capabilities.md) e [solução de problemas](guides/troubleshooting.md) estão em chinês simplificado. O guia de API está em inglês. Uma imagem conceitual não demonstra continuidade temporal, sincronização labial, precisão do modelo nem segurança do processo representado.

Leia as [orientações de contribuição](CONTRIBUTING.md) antes de compartilhar propostas ou mídia. Informe as configurações exatas, as funções das entradas, os direitos de uso, suas observações e, com honestidade, se o exemplo foi testado. Não compartilhe credenciais, documentos privados ou URLs assinadas de mídia que expiram. Use o [formulário de contribuição](.github/ISSUE_TEMPLATE/prompt.yml) para preparar as informações necessárias.

## Sobre a bestimage.ai

A equipe da [bestimage.ai](https://bestimage.ai/) seleciona e mantém esta biblioteca de prompts, conectando fluxos criativos a APIs de modelos de imagem e vídeo.

## Ganhe com o programa de afiliados da bestimage.ai

Você publica tutoriais, prompts ou integrações de API? Participe do [programa de afiliados da bestimage.ai](https://bestimage.ai/affiliate-program/) e receba comissões ao recomendar a bestimage.ai ao seu público.

- **20%** sobre o primeiro pedido pago válido de um usuário indicado.
- **10%** sobre os pedidos pagos válidos seguintes desse usuário, feitos nos **60 dias após o cadastro**.

A elegibilidade dos pedidos e os pagamentos seguem o [contrato de afiliados vigente](https://bestimage.ai/affiliate-agreement/).

## Licença

[MIT](LICENSE).
