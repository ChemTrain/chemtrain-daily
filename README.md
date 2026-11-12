<img src="logo.svg" alt="ChemTrain logo" height="110" align="right">

# ChemTrain Daily

ChemTrain Daily is a daily chemistry quiz, an endless "beast mode" and made-to-order problem sets, built from the questions of every ChemTrain app. Everything is in one HTML file.

**Play it here:** https://chemtrain.github.io/chemtrain-daily/chemtrain_daily.html

You can also download `chemtrain_daily.html` and open it in any browser.

## What's inside

- **Daily quiz:** fifteen questions: four from Reaction Learn (at least two of them naming the reaction), one each from PG Learn and Photoredox Learn, two from each other app, and one more from any app. No two are about the same molecule or reaction, an app's questions are of different kinds where it can, and each app works through its whole pool before a question comes back. Everyone gets the same fifteen on the same day, and a new quiz starts at midnight. Your score, your streak of days and the last week are saved in your browser, and you can copy your result to share it. Past quizzes can be played too, ones you missed or again; they are scored apart and do not count toward your streak.
- **Ranking:** pick a pseudo and today's score joins the boards: today, this week, this month and all time, for everyone or for a group you make and share by link. The same pseudo on another device (a 16-character code links it) brings your scores and your progress in every ChemTrain app along. No email, no password; the server keeps only the pseudo, the scores and the synced progress, and you can delete them any time.
- **TMC questions** come with the d block of the periodic table, the metal of the question marked, as in TMC Learn.
- **Beast mode:** choose all apps or one of them, then answer until your first mistake. Your score is how many you get right in a row; harder questions join after ten. Your best run in each pool is saved.
- **Problem set:** pick any mix of the 32 topics (each app's kinds of question) and how many questions you want, 50, 100, 150 or any number. They are shared equally between your topics, and your progress is saved after every answer. The results show your score by topic, the questions you missed and a set of just those to retry. Share the set's link and everyone who opens it gets the same questions, in the same order with the same choices, so you can compare scores. Reactivity Learn's N and E questions (values, ranking, Reacting?) and Photoredox Learn's cycle and electron-transfer questions are only here, never in the daily quiz or Beast mode.
- About 2,900 questions with their structures and explanations:
  - [pKa Learn](https://github.com/ChemTrain/pka-learn): pKa values, the strongest acid of four, the most acidic proton
  - [Reaction Learn](https://github.com/ChemTrain/reaction-learn): the product of a named reaction, the name of a reaction, the missing reagent
  - [PG Learn](https://github.com/ChemTrain/pg-learn): which protecting group the conditions remove, and which conditions remove a group
  - [TMC Learn](https://github.com/ChemTrain/tmc-learn): electron counts, oxidation states, dⁿ, shapes, ligand electrons and L/X classes
  - [Reactivity Learn](https://github.com/ChemTrain/reactivity-learn): Mayr N and E values, the most nucleophilic or electrophilic of four, whether a pair reacts (these three in problem sets only), the most reactive atom and regioselectivity
  - [Photoredox Learn](https://github.com/ChemTrain/photoredox-learn): redox potentials, the substrate easiest to oxidise or reduce; in problem sets also quenching cycles, the right photocatalyst, turnover and electron-transfer pairs
  - [Radical Learn](https://github.com/ChemTrain/radical-learn): whether a radical is nucleophilic or electrophilic, polarity matching, and where radicals add or take a hydrogen

## How it is built

`src/build.py` reads the data built into each app's page (the local apps, and TMC Learn from GitHub), turns it into one bank of multiple-choice questions, and writes `chemtrain_daily.html`. Rebuild it after an app changes. The daily selection is drawn from the date with a fixed seed, so it is the same for everyone with the same version of the page. A problem-set link lists its questions by their content, not their position, so it keeps working after a rebuild; a question whose text has changed since is left out.

## How to cite

If you use ChemTrain Daily in a course, please cite it and the apps its questions come from:

> Bindschaedler, Q. P. *ChemTrain Daily* (2026). ChemTrain. https://github.com/ChemTrain/chemtrain-daily

## License

- Code (the HTML, CSS and JavaScript): [MIT](LICENSE).
- Content: the questions are built from the content of the ChemTrain apps, each under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): pKa Learn, Reaction Learn, PG Learn, Reactivity Learn, Photoredox Learn and Radical Learn by Quentin Bindschaedler, and TMC Learn by Francesco Sala. See [LICENSE-CONTENT.md](LICENSE-CONTENT.md).
- Logo (`logo.svg`): the locomotive is adapted from [Twemoji](https://github.com/jdecked/twemoji), © Twitter, Inc and other contributors, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); the benzene-ring smoke was added for ChemTrain.
