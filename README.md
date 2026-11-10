# Tatiane Telli, Nutricionista

Página da nutricionista Tatiane Telli (@tellitatiane), pós-graduada em Nutrição Clínica, com consultório no Centro de Salto, SP, e atendimento on-line. Ela não tinha site; esta é a primeira versão, feita do zero.
Versão 1 (10/11/2026), conceito "os bilhetes": abertura em vinho com a foto dela e bilhetes presos com prendedor, bilhete que a paciente monta e vira a mensagem do WhatsApp, mural "Quem é a Tatiane?", avaliações em esteira, planos num varal e mapa do consultório.
HTML, CSS e JavaScript puros, sem build. Todos os botões de agendamento abrem o WhatsApp.

## Estrutura

```
index.html                   página completa (estilos, scripts e logo em SVG dentro do arquivo)
img/tati-hero.png            foto da abertura (gerada por IA com autorização, fundo removido)
img/tati-jaleco.jpg          mural: selfie de jaleco (Instagram)
img/tati-hospital.jpg        mural: no hospital (Instagram)
img/tati-cafe.jpg            mural: cafezinho (Instagram)
img/creme-abacate.jpg        mural: receita do creme de abacate (Instagram)
img/consultorio-mesa.jpg     consultório: mesa (perfil do Google)
img/consultorio-sala.jpg     consultório: sala (perfil do Google)
img/favicon.png              ícone da aba (monograma do logo)
img/apple-touch-icon.png     ícone ao salvar na tela do celular
vercel.json                  configuração da Vercel (URLs limpas)
```

## Publicar

1. Crie um repositório no GitHub (ex.: `Tatiane_Telli`) e envie os arquivos desta pasta para a raiz dele.
   Importante: **arraste a pasta `img` inteira** para a área de upload. O botão "choose your files" não envia pastas.
2. Na Vercel, clique em **Add New → Project**, importe o repositório e mantenha:
   - Project Name: `nutri-tatianetelli`
   - Framework Preset: **Other**
   - Build Command: vazio
   - Output Directory: vazio (raiz)
3. Clique em **Deploy**. O site fica em https://nutri-tatianetelli.vercel.app/ e cada novo commit publica a atualização sozinho.

## Imagens

Ao trocar uma imagem mantendo o mesmo nome, aumente o número `?v=1` nos links do `index.html` (por exemplo `?v=2`) para os navegadores baixarem a versão nova.
A foto da abertura foi gerada no Gemini a partir das fotos dela (original em `previas/tatiane-telli/referencias-ia/`). As fotos do Instagram são de qualidade média.

## Logo

O logo (monograma "T" com ramo e assinatura) está desenhado em SVG dentro do `index.html` (símbolo `i-selo`). Os arquivos em PNG para a cliente usar em outros lugares ficam fora desta pasta, em `previas/tatiane-telli/logo/`.

## Editar conteúdo

- Número do WhatsApp: variável `numero` no fim do `index.html` (hoje 5511958303594) e o número exibido no bilhete final e no rodapé.
- Mensagem padrão: atributo `data-wa` de cada botão. Quando a pessoa marca itens no bilhete, todos os botões passam a enviar "Oi, Tatiane! Vim pelo site e quero começar pelo básico:" com a lista marcada.
- Itens do bilhete: as caixas `<label class="opcao">` da seção `#bilhete` (o `value` é o texto que vai para a mensagem).
- Horários: lista `.horarios` e a regra do "Aberto agora" no fim do script (seg a sex 8h às 18h, sáb 8h às 12h).
- Cores: variáveis no início do `<style>` (`--amora`, `--rose`, `--blush`, `--salvia`, `--esmeralda`).
- Se o endereço final do site mudar, atualize `og:url`, `og:image` e `canonical` no `<head>`.

## A confirmar com a cliente

- Se aprova a foto da abertura gerada por IA (avisar na proposta).
- Se trabalha com consulta e acompanhamentos de 90 e 180 dias.
- CRN (não aparece no site porque não está publicado).
- Se podemos dizer que ela atua em hospital (o site não cita o nome do hospital).
- Logo: a versão do site é uma releitura do logo dela; se tiver o arquivo original em alta resolução, dá para trocar.
