<img src="logo.svg" alt="ChemTrain logo" height="110" align="right">

# ChemTrain Daily

ChemTrain Daily is a daily chemistry quiz and an endless "beast mode", built from the questions of every ChemTrain app. Everything is in one HTML file.

**Play it here:** https://chemtrain.github.io/chemtrain-daily/chemtrain_daily.html

You can also download `chemtrain_daily.html` and open it in any browser.

## What's inside

- **Daily quiz:** ten questions, two from each app. Everyone gets the same ten on the same day, and a new quiz starts at midnight. Your score, your streak of days and the last week are saved in your browser, and you can copy your result to share it.
- **Beast mode:** choose all apps or one of them, then answer until your first mistake. Your score is how many you get right in a row; harder questions join after ten. Your best run in each pool is saved.
- About 2,300 questions with their structures and explanations:
  - [pKa Learn](https://github.com/ChemTrain/pka-learn): pKa values, the strongest acid of four, the most acidic proton
  - [Reaction Learn](https://github.com/ChemTrain/reaction-learn): the product of a named reaction, the name of a reaction, the missing reagent
  - [PG Learn](https://github.com/ChemTrain/pg-learn): which protecting group the conditions remove, and which conditions remove a group
  - [TMC Learn](https://github.com/ChemTrain/tmc-learn): electron counts, oxidation states, dⁿ, shapes, ligand electrons and L/X classes
  - [Reactivity Learn](https://github.com/ChemTrain/reactivity-learn): Mayr N and E values, the most nucleophilic or electrophilic of four, whether a pair reacts, the most reactive atom, and regioselectivity

## How it is built

`src/build.py` reads the data built into each app's page (the four local apps, and TMC Learn from GitHub), turns it into one bank of multiple-choice questions, and writes `chemtrain_daily.html`. Rebuild it after an app changes. The daily selection is drawn from the date with a fixed seed, so it is the same for everyone with the same version of the page.

## How to cite

If you use ChemTrain Daily in a course, please cite it and the apps its questions come from:

> Bindschaedler, Q. *ChemTrain Daily* (2026). ChemTrain. https://github.com/ChemTrain/chemtrain-daily

## License

- Code (the HTML, CSS and JavaScript): [MIT](LICENSE).
- Content: the questions are built from the content of the ChemTrain apps, each under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): pKa Learn, Reaction Learn, PG Learn and Reactivity Learn by Quentin Bindschaedler, and TMC Learn by Francesco Sala. See [LICENSE-CONTENT.md](LICENSE-CONTENT.md).
- Logo (`logo.svg`): the locomotive is adapted from [Twemoji](https://github.com/jdecked/twemoji), © Twitter, Inc and other contributors, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); the benzene-ring smoke was added for ChemTrain.
