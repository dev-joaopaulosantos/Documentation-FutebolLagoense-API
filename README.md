# API Futebol Lagoense

## http://futebol-lagoense.vercel.app

#### Retorna um array com todos os campeonatos cadastrados no banco de dados

```http
  GET /api/championships

```
Cada campeonato possui:
| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `_id`      | `ObjectID` | ID do campeonato  |
| `name`      | `String` | Nome do campeonato |
| `year`      | `Date` | Ano do campeonato |
| `image`      | `String` | Link da logo do campeonato |
| `groupStage`      | `Boolean` | Mostra se o camp. tem fase de grupos |
| `champion`      | `String` | Vencedor do campeonato |
| `award`      | `String` | Premiação do campeonato |
| `secondPlace`      | `String` | Segundo colocado do campeonato |
| `thirdPlace`      | `String` | Terceiro colocado do campeonato |
| `goalScorer`      | `String` | Artilheiro do campeonato |
| `bestPlayer`      | `String` | Melhor jogador do campeonato |
| `bestGoalkeeper`      | `String` | Melhor goleiro do campeonato |


#### Retorna todos as equipes cadastradas no banco de dados

```http
  GET /api/teams
```

Cada equipe possui:
| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `_id`      | `ObjectID` | ID da equipe  |
| `name`      | `String` | Nome da equipe|
| `shield`      | `String` | Link do escudo da equipe|

#### Retorna um array com todas as equipes de um determinado campeonato

```http
  GET /api/team/${id}
```

#### Retorna um array com todos os jogos de um determinado campeonato

```http
  GET /api/games/${id}
```
Cada jogo possui:
| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `_id`      | `ObjectID` | ID do jogo  |
| `date`      | `Date` | Data do jogo|
| `local`      | `String` | Local onde a partida vai ocorrer|
| `phase`      | `Number` | Fase do camp. em que a partida vai ocorrer|
| `round`      | `Number` | Rodada em que a partida vai ocorrer|
| `gameInfo`      | `String` | Informação do jogo|
| `matchStatus`      | `String` | Status da partida|
| `homeTeam.name`      | `String` | Nome da equipe mandante|
| `homeTeam.shield`      | `String` | Link do escudo da equipe mandante|
| `awayTeam.name`      | `String` | Nome da equipe visitante|
| `awayTeam.shield`      | `String` | Link do escudo da equipe visitante|
| `homeGoals`      | `Number` | Gols da equipe mandante|
| `awayGoals`      | `Number` | Gols da equipe visitante|
| `penaltyStatus`      | `Boolean` | Status de penaltes|
| `penaltyGoalsHome`      | `Number` | Gols de penaltis da equipe mandante|
| `awayPenaltyGoals`      | `Number` | Gols de penaltis da equipe visitante|

#### Retorna apenas um jogo de um determinado campeonato

```http
  GET /api/onegame/${id}
```

#### Retorna um array com as classificação de um determinado campeonato

```http
  GET /api/classification/${id}
```
Cada classificação possui:
| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `_id`      | `ObjectID` | ID da classificação  |
| `team`      | `String` | Equipe|
| `group`      | `Number` | Grupo em que a equipe faz parte|
| `games`      | `Number` | Jogos|
| `points`      | `Number` | Pontos|
| `goalsScored`      | `Number` | Gols feitos|
| `goalsConceded`      | `Number` | Gols sofridos|
| `goalDifference`      | `Number` | Saldo de gols|

