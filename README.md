# DraftJS: Export ContentState to HTML

This is a module for [DraftJS](https://github.com/facebook/draft-js) that will export your editor content to semantic HTML.

It was extracted from [React-RTE](https://react-rte.org) and placed into a separate module for more general use. Hopefully it can be helpful in your projects.

## Installation

    npm install --save draft-js-export-html

## How to Use

    import {stateToHTML} from 'draft-js-export-html';
    let html = stateToHTML(contentState);

`stateToHTML` also accepts an optional second argument, a map of entity types and functions which can facilitate rendering:

    let html = stateToHTML(contentState, {
      BOLD: (content) => `<span style="font-weight: bold">${content}</span>`,
      UNDERLINE: (content) => `<span style="border-bottom: 1px solid black">${content}</span>`
    });

This project is still under development. If you want to help out, please open an issue to discuss or join us on [Slack](https://draftjs.slack.com/).

## Contributions

This repo is the
[latest commit of draft-js-export-html](https://github.com/sstur/draft-js-export-html/commit/08b589b4a888168fe43233bfa844ce477d4b314e)
with the following commits from pull requests merged:

* [varun-raj/draft-js-export-html 31f51a3](https://github.com/sstur/draft-js-export-html/pull/22/commits/31f51a3fe02230591067908f77746f0aba112849)
* [xarg/draft-js-export-html 8dbf7fd](https://github.com/sstur/draft-js-export-html/pull/19/commits/8dbf7fdc57393b5a803b9c35571c4153f533002e)
* [nmaquet/draft-js-export-html 98bfac1](https://github.com/sstur/draft-js-export-html/pull/12/commits/98bfac11777b6b59fd84ca98a72faee1bce4fe2c)

## License

This software is [BSD Licensed](/LICENSE).
