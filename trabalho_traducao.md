# Detecção automática de (potenciais) fatores no texto fonte contribuindo para o viés de gênero na tradução automática

## Resumo

Esse projeto de pesquisa busca desenvolver uma metodologia abrangente para ajudar sistemas de tradução automática (TA) terem mais inclusão de gênero para a sociedade.
O objeto é a criação de um sistema de detecção, um modelo de aprendizado de máquina (AM) treinado a partir de anotações manuais, que consegue analisar o dado fonte e destacar palavras e frases que influenciam a inclinação por vieses de gênero na tradução esperada.
Os principais resultados da pesquisa serão (1) uma amostra de dados anotados manualmente, (2) uma taxonomia, e (3) um modelo refinado.

## Créditos

Esse projeto é uma pesquisa estratégica de PhD básica totalmente custeada pela Fundação de Pesquisa - Flanders (FWO) dura o período de quatro anos de 11.01.2023 até 31.10.2027, e hospedada dentro da Equipe de Tecnologia de Linguagem e Tradução (LT3) na Universidade de Ghent.

## Introdução

Com o crescimento do uso e interesse no desenvolvimento da tradução automática (TA) e a crescente demanda por mais inclusão de gênero na sociedade, pesquisa no viés de gênero na TA está aumentando (Salvodi et al., 2021).
Um sistema de AT é considerado enviesado de gênero se ele "descrimina sistematicamente e injustamente certos indivíduos ou grupos em favor de outros" (Salvodi et al., 2021, p. 846), perpetuando "estereótipos incorretos e potencialmente discriminatórios" na sociedade (Vanmassenhove, 2024, p. 3).
Estudos de nível global mostram que a incorporação de palavras usada no treinamento de TA são altamente influenciadas por gênero, onde incorporação de palavras de diferentes classes gramaticais se acumulam baseado no seu gênero em diferentes domínios (p. ex., em esportes, cozinha, gigantes da tecnologia, profanidades sexuais) (Caliskan et al., 2022).
Entretanto, o estudo de incorporações de palavras é limitado a uma análise em nível global e ainda abrange o <!-- não foi estendido ao --> contexto total das fontes de frase em linguagem natural e as resultantes associações de gênero na tradução automática.

## Descrição do Projeto

Nesse projeto de pesquisa, aplicamos uma abordagem inovadora para analisar características linguísticas e morfológicas alinhadas, com um foco no gênero na fonte e identificar textos e aplicar metodologias de aprendizado de máquina.
Inglês foi escolhido como idioma fonte, onde substantivos de papel do sujeito geralmente não são marcados por gênero (p. ex. teacher) e as traduções alvo são analisadas em alemão e espanhol, idiomas com gênero gramático (Savoldi el al., 2021), onde o gênero é marcado claramente (p. ex. Lehrer/Lehrerin).
O foco é identificar e classificar automaticamente "palavras gatilho" em um contexto fonte que influencie inflexões gramaticais de gênero na tradução alvo (ou seja, sempre que ama AT traduzir uma pessoa como homem ou mulher, ou em vez disso prefira neutralizar ou refrasear a palavra).
O projeto consiste dos seguintes entregáveis principais que diferem do estudo estudo anterior: (1) um conjunto de dados feitos manualmente de associações de gêneros no contexto da frase, (2) uma taxonomia baseada nesses dados, (3) uma análise comparativa das associações de gênero humanas vs. as inflexões de gênero da AT, e (4) um grande modelo de linguagem (LLM) refinado que destaque palavras de gatilho para gênero no texto fonte.

### Coleta de dados

O primeiro passo é a coleta de de uma lista de palavras candidatas (papeis, nomes, p. ex. friend) incluindo suas inflexões de gênero, amostrada de suas incorporações em estudos anteriores.
Essas palavras são usadas para filtrar dados de inglês mono-lingual de diferentes domínios, lembrando levemente a metodologia usada por Ondoño-Soler e Forcada (2022).
Seguido da filtragem automática, as frases em inglês são filtradas manualmente em um nível mono-lingual para selecionar casos de ambiguidade de gênero da palavra candidata isolada. 
Nosso objetivo é de 2.000 a 5.000 frases para o modelo refinado.
Seguindo, os dados filtrados serão traduzidos automaticamente para o alemão e espanhol usando ferramentas de AT disponíveis ao público.
Nos documentamos e comparamos para qual gênero o sistema de AT traduz cada palavra candidata, primeiro em um nível de palavra (p. ex. o termo individual friend) e depois em um contexto de frase (p. ex. After a friend suggested she try it, Ann said, "Sure!").
Os dois registros de texto bilíngue (IN-AL, IN-ES) serão alinhados e enriquecidos em nível de palavra por informações morfosintaticas.


