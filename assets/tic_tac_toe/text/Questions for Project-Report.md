Questions for Project-Report

What question you are looking to answer?
Kann ich ein einfaches tic tac toe spiel in pygame implementeiren? kann ich es visuell ansprechend gestalten? Kann ich verschiedene KI Gegner implementieren?

Why does this question matter?
Ich möchte mein Können in den Bereichen Spieleentwickluong, Visualisierung und KI erweitern.

What code did you write / use?
ich habe in pygame das spiel tic tac toe programmiert. und anschließend 3 verschiedene KI Gegner implementiert.
Eine Ki, die zufällig Züge wählt, eine KI, die per Reinforcement Learning lernt und eine KI, die die minimax STrategie nutzt

How did you fit the model?
Ich habe als reinforcement learning agenten q learning verwendet. der q learning agent hat 1 Mio tic tac toe spiele gegen sich selbst gespielt und dabei über 800 SPielsituationen erfasst.

How did you validated the model?
ich habe zum einen selber gegen die Gegner gespielt, aber auch die gegner gegeneienander antreten lassen. die ergebnisse hierzu habe ich in einer streamlit app veröffentlicht. unter den angegebeben links kann aber auch jeder selbst gegen den jeweilgien KI Gegner spielen

How you know the results make sense?
Der Schwierigkeitsgrad der Gegner nimmt sukzessive zu. Am leichtesten ist der random Gegener, danach q learning, welcher jedoch nur wenig besser ist. Am besten ist der minimax gegner, da dieser bei der beschränkten auswahl von möglichkeiten in tic tac toe immer den optimalen PFad wählt, weil er immer alle zukünftigen Spielzustände verausberechnen kann.

How did you visualized the results?
Ich visualisiere zum einen in oygame um dort das spiel zu zeigen. außerdem habe ich stramlit genutzt, um die ergebnisse der spiele der KI Gegner gegeneinander abzubilden. HIerfür nutze ich diagramme, die ich it matplotlib erstellt habe.

What did you learn?
Ich hatte das erste mal berührung mit reinforcement learning und der Erstellung von KI Gegnern. Auch das Turnier, in dem die KI Gegner gegeneinander angetreten sind, war neu für mich. Ich habe außerdem zum ersten mal eine streamlit app deployed.

