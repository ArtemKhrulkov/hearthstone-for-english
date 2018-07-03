# Hearthstone For English
Итак, представляем вам очередную реализацию Hearthstone, только теперь с более интересной механикой :)

## Краткое описания процесса игры:
- Игра делится на раунды
- За каждый удачный ход игроку даётся жетон или отнимается HP у противника. "Удачным ходом" считается ход, в котором игрок 
смог удачно выполнить заклинание/действие направленное либо на себя (без негативного эффекта), либо на противника.
- Каждому игроку выдаётся по 4 карты
- В центре доски находится языковой паттерн (например, SVO - Subject, Verb, Objective,
что означает Подлежащее, Сказуемое и Дополнение)
- Игроки по очереди выкладывают карты в порядке языкового паттерна. Каждая карта подписана, к какому порядку она относится 
(например, все сказуемые подписаны буквой V, все подлежащие - буквой S и т.д.). У каждой карты сказуемого есть своё описание, 
что она делает и какова продолжительность эффекта. Если у игрока есть полная комбинация совпадающая с паттерном,
то он может выложить всю комбинацию сразу
- Карты и колоду можно сбрасывать 3 раза за рануд
- Игроки ходят до тех пор пока не заполнится языковой паттерн. Как только это произойдёт, то игроки продолжают играть,
пока кто-либо из них не сделает пас. Когда один из игроков сдался, эффект который будет выложен в паттерне, выполняется
и раунд будет считаться законченным
- Игра продолжается до набора 5 жетонов или победы одного из игроков

## Языковые паттерны
Здесь будут перечилсенны языковые паттерны которые будут участвовать в игре
1. `SVO` (Подлежащее, Сказуемое и Дополнение)
2. `SVO&A` (Подлежащее, Сказуемое, Дополнение с Определением)
3. `CSVO` (Обстоятелсьтво(например,вчера), Подлежащее, Сказуемое, Дополнение с Определением)
4.  `S|AuV+not|VO` (тоже что и SVO, только с вспомогательным глаголом и частицой not)
5. `S|AuV|VO` (тоже самое что и SVO, только с вспомогательным глаголом (например, will))
