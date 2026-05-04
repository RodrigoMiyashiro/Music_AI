# Planejamento do Aplicativo Music AI

## Visao do produto

Aplicativo mobile de descoberta musical e organizacao pessoal, usando o MusicBrainz como fonte principal de metadados (artistas, lancamentos, gravacoes, relacoes e creditos).

- Foco: descoberta e contexto musical.
- Nao foco: streaming nativo de audio.

## Problema que o app resolve

- Facilitar exploracao de discografias e versoes de albuns.
- Organizar interesse do usuario (favoritos, quero ouvir, historico).
- Gerar retorno ao app com alertas e trilhas de descoberta.

## Funcionalidades principais

### 1) Busca inteligente

- Busca unica para artista, album, faixa e selo.
- Resultados separados por categoria (Artistas, Lancamentos, Gravacoes).
- Filtros: pais, ano, tipo (album/single/EP), status (official/bootleg).

### 2) Perfil de artista

- Dados basicos: nome, pais, periodo de atividade, aliases.
- Discografia por tipo de lancamento.
- Relacoes relevantes (colaboracoes, projetos, labels).

### 3) Detalhe de lancamento

- Informacoes de edicao: data, pais, formato, selo e tracklist.
- Diferencas entre versoes (ordem de faixas, bonus tracks, duracao).

### 4) Comparador de edicoes

- Compara duas versoes lado a lado.
- Destaque visual para diferencas de metadados e faixas.

### 5) Colecao pessoal

- Marcacoes: Tenho, Quero ouvir, Favorito, Ouvido.
- Listas customizadas para organizar descobertas.

### 6) Seguir artista e alertas

- Seguir artistas para receber atualizacoes de novos lancamentos.
- Preferencias de alerta por tipo de release.

### 7) Descoberta relacionada

- Sugestoes baseadas em tags, relacoes e colaboracoes.
- Evolucao futura para recomendacao hibrida (regra + comportamento).

## Relacao entre funcionalidades (fluxo)

1. Usuario entra pela Home.
2. Explora artistas/lancamentos em destaque.
3. Abre perfil de artista e detalhe de lancamento.
4. Salva itens na colecao pessoal.
5. Segue artistas para receber alertas.
6. Retorna via notificacoes e continua descoberta.

Esse ciclo cria retencao: descoberta -> organizacao -> reengajamento.

## Home inicial sem busca (antes de qualquer interacao)

Como o MusicBrainz nao fornece ranking oficial de popularidade, a Home deve combinar curadoria e dinamismo.

### Secoes sugeridas para a primeira tela

1. Em destaque (Top 10 curado) [MVP recomendado]
   - Lista fixa inicial de 10 artistas (config local ou backend).
   - Objetivo: causar boa primeira impressao e orientar descoberta.

2. Lancamentos recentes
   - Lista de releases recentes para trazer conteudo vivo.

3. Explorar por genero/tag
   - Blocos por tema para descoberta rapida.

4. Continuar explorando (quando houver historico)
   - Ultimos vistos, favoritos e itens da lista Quero ouvir.

## MVP recomendado

- Busca inteligente
- Perfil de artista
- Detalhe de lancamento
- Colecao pessoal (Favorito e Quero ouvir)
- Home com Top 10 curado + Lancamentos recentes

## Integracoes complementares

- Cover Art Archive para imagens de capa.
- Backend leve para cache, normalizacao e controle de rate limit.

## Indicadores de sucesso

- Taxa de retorno semanal (WAU/MAU).
- Itens salvos por usuario (favoritos/quero ouvir).
- Cliques em recomendacoes relacionadas.
- Conversao de Home -> detalhe de artista/lancamento.

## Proximos passos tecnicos

1. Definir stack mobile (Flutter, React Native ou KMP).
2. Especificar contratos de dados da Home e da Busca.
3. Implementar camada de API + cache local.
4. Entregar prototipo navegavel da Home e Detalhe.
