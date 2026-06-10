# Language packs for [QuizTools](https://github.com/fsvblr/quiztools)

List of available language packs for **QuizTools** package: https://fsvblr.github.io/quiztools-languages/.

Project on [crowdin.com](https://crowdin.com/project/quiztools). [![Crowdin](https://badges.crowdin.net/quiztools/localized.svg)](https://crowdin.com/project/quiztools)<br>
You can participate in translating the package into your language at **Crowdin**. If your language isn't listed, please submit a "Request New Language" through the Crowdin interface.

## Localization Contributors

A huge thank you to the wonderful people who help bring **QuizTools** to users around the world!

| Language | Contributors |
| :--- | :--- |
| 🇫🇷 **French (fr-FR)** | Vincent Ferrari |
| 🇮🇹 **Italian (it-IT)** | Vincent Ferrari |

## Notes:
- The current Crowdin settings send all project files and strings, including untranslated ones. Untranslated strings are in the English localization. This matches Joomla's default behavior. If change the Crowdin settings by selecting the "Skip untranslated strings" option, it will be difficult (though possible) to correct previously translated strings. Crowdin doesn't see the changes (they were "translated" and remain "translated").


## License

This project is released under the [GPL v2](LICENSE).  

## Flow
### Translation has changed on Crowdin:
- File changes in crowdin.com automatically create a pull request here. Crowdin and GitHub sync every 1 hour.
- Review before merging: Translations are pushed to a service branch (l10n), allowing to verify changes via Pull Request before merging into target branch.
- After the PR is merged, the following happens automatically:
  - A new version of the package for the changed language is built, a release is created, and the package is attached to it.
  - The download link for the changed package in [the package list](https://fsvblr.github.io/quiztools-languages/) is updated.
  - The update server XML file is updated.
- Branch cleanup: Delete the l10n branch after merging to prevent conflicts. Crowdin will automatically recreate it when new translations are ready.
- Add to the "Localization Contributors" block.

### After receiving a request from Crowdin to add a language:
- Create a language folder.
- Place the XML manifest in it.
- Add the language block (alphabetically) to index.html.
- Add the {{ lang }}.xml template-file on the update server
- Add the language to Crowdin
