# TREINO

Registo de treinos para o Eduardo e a Maria. Ficheiro único, sem servidor, sem contas.

**Live:** `https://<username>.github.io/treino/`

## O que faz

- **Min-Max 4X** (Jeff Nippard): 4 dias (Full Body, Upper, Lower, Arms/Delts), séries, repetições, RIR por semana (1 a 12), técnicas de intensidade a partir da semana 8, e link para o vídeo de demonstração de cada exercício.
- **Total Abs** (Darebee): 30 dias, níveis I/II/III.
- **Daily Reps**: circuito opcional de 6 movimentos, 3 rondas, para casa.
- **Sessão livre**: corrida, bicicleta, outros. Com opção "isto foi aquecimento" (conta minutos, não conta como sessão).
- **Cronómetro de descanso**: 1:00 / 1:30 / 2:00 / 3:00 / 5:00, com vibração e som no fim.
- **Semana**: mostra os dias de treino da semana e permite começar qualquer um.
- **Dois perfis**: Eduardo (com horário por turnos) e Maria (sem horário fixo). Históricos totalmente separados.

## Regra importante: rotação, não datas fixas

O treino do dia **não está preso à data**. É sempre o seguinte na rotação
(Full Body, Upper, Lower, Arms) a contar do último Min-Max registado.

Se falhares um treino, ele **desliza** para o próximo dia disponível em vez de ser saltado.
Por isso nunca se repete o mesmo treino nem se perde nenhum.

O calendário diz **quando**; a app diz **o quê**.

## Instalar no telemóvel

1. Abrir o link no Chrome
2. Menu ⋮ → **Adicionar ao ecrã principal**
3. Escolher o cartão (Eduardo ou Maria) na primeira utilização

## Onde ficam os dados

No armazenamento do próprio browser (`localStorage`), por telemóvel.
Não há sincronização entre dispositivos: o telemóvel do Eduardo e o da Maria
têm históricos independentes, o que é exatamente o pretendido.

**Cópia de segurança:** separador Histórico → **Export** → guardar o texto.
Para restaurar (telemóvel novo, dados apagados): colar o texto → **Import**.
Vale a pena fazer isto de vez em quando: limpar os dados do site apaga o histórico.

## Actualizar

Substituir o `index.html` no repositório. O URL e o armazenamento mantêm-se,
por isso o histórico sobrevive às actualizações.

## Manutenção mensal

Os dias de treino do Eduardo estão no objecto `SLOTS` dentro do `index.html`,
gerados a partir da escala do mês (CUF Porto). Regras usadas:

- Nunca treinar na manhã a seguir a uma noite (sai às 8h30, isso é para dormir)
- Dia "D" (8h-20h30) é dia de descanso
- Turno "M" (8h-14h30) permite treinar às 17h
- Turnos "N" e "TN" permitem treinar de manhã, mas **moderado**
- Alvo: 4 sessões por semana, a descer para 3 em semanas muito pesadas

O perfil da Maria tem `SLOTS.maria = {}` (vazio), o que significa que todos os
dias estão disponíveis.
