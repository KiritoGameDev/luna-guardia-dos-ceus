# Luna: Guardiã dos Céus

> Jogo 3D de voo arcade no navegador. Atravesse anéis de luz, desvie de obstáculos, derrote chefes e evolua sua nave por 14 céus, cada um com cenário, clima e trilha sonora próprios.

**Jogar:** `https://SEU-USUARIO.itch.io/luna-guardia-dos-ceus` _(troque pelo link da sua página)_
**Idiomas:** Português · English · Español
**Plataformas:** navegador (computador e celular) · **Versão:** 1.0.0

[English version → README.en.md](README.en.md) · [Documento completo do projeto → docs/DOCUMENTO_DO_PROJETO.md](docs/DOCUMENTO_DO_PROJETO.md)

<!-- Coloque aqui 3 a 4 screenshots, por exemplo: -->
<!-- ![Fase 2 - Noite de Chuva](docs/screenshots/fase2.png) -->

---

## Sobre

Você é **Luna**, a mais jovem piloto do reino de Aurora. O Cristal das Estrelas foi quebrado pelo **Eclipse Sombrio** e seus 11 fragmentos de luz se espalharam pelos céus. Cruze cada céu, reúna os fragmentos e junte as engrenagens que transformam a sua nave.

O jogo roda inteiro em **um único arquivo HTML** com **Three.js** (WebGL). Não usa imagens, modelos 3D nem arquivos de áudio externos: os cenários, as naves e as **músicas são gerados por código**.

## Destaques

- **14 fases:** 11 da campanha e 3 mundos bônus liberados ao zerar o jogo.
- **15 trilhas procedurais** (14 fases + tema do menu), que aceleram no meio e no fim de cada fase.
- **Clima dinâmico:** chuva, neve, raios, meteoros, brasas, pétalas, aurora boreal e bolhas.
- **3 lutas de chefe:** dois mini-chefes (fases 5 e 8) e o chefe final, o Eclipse.
- **6 naves** com habilidades únicas, cada uma com **12 formas** que evoluem conforme você coleta engrenagens.
- **Loja, estrelas por fase, missões diárias e Modo Infinito.**
- **Ranking** de campanha e de Infinito.
- **Acessibilidade:** aviso de fotossensibilidade, opção de reduzir flashes, 3 idiomas, volumes separados e vibração configurável.

## Como jogar

| Ação | Computador | Celular |
|---|---|---|
| Mover a nave | Mouse, setas ou WASD | Arrastar o dedo |
| Dash (nave Cometa) | Barra de espaço | Botão DASH |
| Pausar | `P`, `Esc` ou botão **II** | Botão **II** |
| Música ligada/desligada | `M` | Opções |

**Objetivo:** sobreviva até a barra de progresso encher e atravesse os anéis. Dourado vale 10 pontos, azul 25, rosa 50, e o anel arco-íris vale 100 pontos e +1 vida. Pegue as 2 engrenagens verdes de cada fase para evoluir a nave. Nas lutas de chefe, os anéis machucam o inimigo.

## Conteúdo

| # | Fase | Clima / destaque | BPM |
|---|---|---|---|
| 1 | Amanhecer Dourado | Sol gigante | 118 |
| 2 | Noite de Chuva | Lua, chuva e estrelas | 92 |
| 3 | Vale Congelado | Neve | 80 |
| 4 | Chuva de Meteoros | Meteoros | 142 |
| 5 | Tempestade Elétrica | Raios · **mini-chefe: Espectro da Tempestade** | 150 |
| 6 | Jardim das Cerejeiras | Pétalas | 108 |
| 7 | Aurora Boreal | Aurora e estrelas | 100 |
| 8 | Montanha de Lava | Brasas · **mini-chefe: Golem de Lava** | 132 |
| 9 | Lua de Cristal | Lua gigante | 116 |
| 10 | Eclipse Sombrio | Sol negro, raios e meteoros | 126 |
| 11 | Templo das Estrelas | **Chefe final: Eclipse, o Devorador de Estrelas** | 132 |
| 12 | Recife Profundo _(bônus)_ | Fundo do mar e bolhas | 104 |
| 13 | Cidade Neon _(bônus)_ | Céu neon, baixo pulsante | 118 |
| 14 | Espaço Profundo _(bônus)_ | Planeta gigante e meteoros | 96 |

### Naves

| Nave | Preço (★) | Habilidade |
|---|---|---|
| Aurora | Grátis | +0,4 s de invencibilidade após bater |
| Falcão | 500 | Controle bem mais rápido |
| Manta | 4.000 | Ímã passivo que atrai anéis |
| Cometa | 11.000 | Dash invencível (recarga de 12 s) |
| Fênix | 24.000 | Renasce uma vez por fase |
| Dragão | 50.000 | Escudo de fogo (absorve 1 batida a cada 25 s) |

## Tecnologias

- **HTML5 + JavaScript** (sem build, sem framework)
- **[Three.js r128](https://threejs.org/)** para o 3D (WebGL)
- **Web Audio API** para o sequenciador e os sintetizadores das músicas
- **localStorage** para salvar progresso, loja, missões e configurações

## Executar localmente

Não há dependências para instalar. Basta abrir o `index.html` no navegador, ou servir a pasta:

```bash
# na raiz do repositório
python3 -m http.server 8000
# abra http://localhost:8000
```

## Estrutura do repositório

```
.
├── index.html            # o jogo inteiro (código, estilos e o retrato da Luna embutido)
├── lib/
│   └── three.min.js      # Three.js r128 (MIT)
├── docs/
│   ├── DOCUMENTO_DO_PROJETO.md
│   ├── ITCH_IO.md        # textos e configurações da página do itch.io
│   └── screenshots/      # coloque aqui as capturas de tela
├── README.md
└── README.en.md
```

## Créditos

- **Criador e Desenvolvedor:** Dragon
- **Estúdio:** Dragon Slayer Studio
- **Three.js:** © Three.js Authors, licença MIT.
- O desenvolvimento do código foi assistido por IA (Claude, da Anthropic). Veja a seção _Créditos e licenças_ do [documento do projeto](docs/DOCUMENTO_DO_PROJETO.md).

## Licença

_Defina aqui a licença do seu código (por exemplo MIT) e a dos seus ativos._ O Three.js é distribuído sob licença MIT.
