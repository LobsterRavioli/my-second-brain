---
tags:
  - commands
type: gnu_and_unix_commands
description: split bash mirror in more screen
Date: 2024-09-18 17:09
weight: "4"
---

___
# tmux

## Syntax
```bash
tmux 
```

## Description
Ecco il **cheat sheet di tmux** formattato in una tabella per una consultazione rapida:

| **Azione**                               | **Comando**                          |
|------------------------------------------|--------------------------------------|
| **Avviare una nuova sessione**           | `tmux`                               |
| **Avviare una nuova sessione con nome**  | `tmux new -s session_name`           |
| **Elencare tutte le sessioni**           | `tmux ls`                            |
| **Agganciarsi a una sessione esistente** | `tmux attach -t session_name`        |
| **Staccare una sessione**                | `Ctrl + B`, quindi `D`               |
| **Terminare una sessione**               | `tmux kill-session -t session_name`  |
| **Creare una nuova finestra**            | `Ctrl + B`, quindi `C`               |
| **Visualizzare l'elenco delle finestre** | `Ctrl + B`, quindi `W`               |
| **Spostarsi alla prossima finestra**     | `Ctrl + B`, quindi `N`               |
| **Spostarsi alla finestra precedente**   | `Ctrl + B`, quindi `P`               |
| **Spostarsi a una finestra per numero**  | `Ctrl + B`, quindi `[numero]`        |
| **Rinominare la finestra corrente**      | `Ctrl + B`, quindi `,`               |
| **Chiudere la finestra corrente**        | `exit`                               |
| **Dividere il pannello in verticale**    | `Ctrl + B`, quindi `%`               |
| **Dividere il pannello in orizzontale**  | `Ctrl + B`, quindi `"`               |
| **Spostarsi al prossimo pannello**       | `Ctrl + B`, quindi `O`               |
| **Spostarsi tra i pannelli (frecce)**    | `Ctrl + B`, quindi frecce direzionali |
| **Chiudere il pannello corrente**        | `Ctrl + B`, quindi `X`               |
| **Ridimensionare pannello (ridurre)**    | `Ctrl + B`, quindi `:resize-pane -L` (or `-D`) |
| **Ridimensionare pannello (aumentare)**  | `Ctrl + B`, quindi `:resize-pane -R` (or `-U`) |
| **Creare una nuova sessione da tmux**    | `Ctrl + B`, quindi `:new-session -s session_name` |
| **Cambiare sessione**                    | `Ctrl + B`, quindi `S`               |
| **Attaccarsi a una sessione da tmux**    | `Ctrl + B`, quindi `:attach -t session_name` |
| **Entrare in modalità copia**            | `Ctrl + B`, quindi `[`               |
| **Muoversi nel testo**                   | Frecce direzionali                   |
| **Iniziare selezione del testo**         | `Ctrl + Spazio`                      |
| **Copiare il testo selezionato**         | `Ctrl + W` o `Invio`                 |
| **Incollare il testo copiato**           | `Ctrl + B`, quindi `]`               |
| **Ricaricare configurazione**            | `Ctrl + B`, quindi `:source-file ~/.tmux.conf` |
| **Chiudere tutti i pannelli tranne uno** | `Ctrl + B`, quindi `:kill-pane -a`   |
| **Visualizzare il tempo**                | `Ctrl + B`, quindi `T`               |

Questa tabella riassume le operazioni principali di tmux per gestire sessioni, finestre e pannelli.
## Option

| Option | functionallity |
| ------ | -------------- |
|        |                |


## Examples
- Create a session
```bash
tmux new -s "LPI" -n "Window zero"
```
- List all sessions
```bash
tmux ls
```

- Kill a session
```bash
tmux kill-session -t "Second Session"**
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]