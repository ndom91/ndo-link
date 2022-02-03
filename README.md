# URL Shortener

Based on Kent C. Dodd's [netlify-shortener](https://github.com/kentcdodds/netlify-shortener).

## 🚀 Usage

1. Run the following command.

```bash
$ npm run shorten [url] [short-code]
```

For example:

```bash
$ npm run shorten https://github.com/ndom91 gh
```

### 🐚 Shell Function

To setup a shell alias to be able to shorten URLs from anywhere, first add the `bin` section to your `package.json`.

```js
{
  "bin": {
    "shorten": "cli.js"
  }
}
```

Then create the `cli.js` file with the following contents.

```js
#!/usr/bin/env node

require("netlify-shortener");
```

Finally, run this from your project's root directory to register the `shorten` alias.

```bash
$ npm link
```

Then you can run `shorten [url] [short-code]` from anywhere in your terminal!

## 📝 License

MIT
