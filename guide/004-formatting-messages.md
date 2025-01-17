# Formatting Messages

Formatting messages allows you to enhance the appearance of text or messages sent by your Telegram bot. You can use Markdown, HTML, MarkdownV2 formatting to style the text, add links, make text bold, italic, or monospaced, create lists, and [more](https://core.telegram.org/bots/api#formatting-options).

## Formatting in telegraf
There are various ways in which you can format the messages in telegraf

- Inbuilt functions
  - `replyWithMarkdown` (deprecated)
  - `replyWithMarkdownV2`
  - `replyWithHTML`
- Extras
  - parse_mode
- Libraries
  - telegraf/format

```js
//Use inbuilt function
ctx.replyWithMarkdownV2('*Hello World*')

//Using parse_mode
ctx.reply('Hello World', {
  parse_mode: 'MarkdownV2'
})
```

## Formatting reference

### Markdown

- Bold Text
  - Wrap the text with <b>*</b>
- Italic Text
  - Wrap the text with *_*
- Monospaced Text
  - Wrap the text with *`*
- Hyperlinked text
  - Create links with `[text](URL)`

More on this [here](https://core.telegram.org/bots/api#markdown-style)

## MarkdownV2
- Bold Text
  - Wrap the text with <b>*</b>
- Italic Text
  - Wrap the text with *_*
- Underlined Text
  - Wrap the text with *__*
- Monospaced Text
  - Wrap the text with *`*
- Spoiler Text
  - Wrap the text with *||*
- Strikethrough text
  - Wrap the text with *~*
- Hyperlinked text
  - Create links with `[text](URL)`

More on this [here](https://core.telegram.org/bots/api#markdownv2-style)

### HTML Formatting

- Bold Text
  - Wrap the text with `<b>` and `</b>`
- Italic Text
  - Wrap the text with `<i>` and `</i>`
- Underlined Text
  - Wrap the text with `<u>` and `</u>`
- Monospaced Text
  - Wrap the text with `<code>` and `</code>``
- Spoiler Text
  - Wrap the text with `<tg-spoiler>` and `</tg-spoiler>`
- Hyperlinked text
  - Create links with `<a href='URL'>text</a>`

More on this [here](https://core.telegram.org/bots/api#html-style)

> Don't forget to precede the required characters for each of the parse modes. 
