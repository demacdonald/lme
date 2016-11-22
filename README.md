![](https://raw.githubusercontent.com/vajahath/lme/master/media/logo.png)

**`console.log` ging done right, beautifully.**


You don't have to write the 13 char long `console.log()` anymore. Try:

```javascript
lme.d("hello world");
```

## Why `lme` *( logme )*
- Simpler to use than `console.log()` or even `console.log(chalk.red("hi"));`
- **Draw lines** with just a single function, [`lme.line()`](#drawing-lines-with-lmeline).
- Automatically expands `objects` and `arrays`. So that, you don't have to use `JSON.stringify()` anymore.
- Clean and semantically focused.
- Actively maintained.
- Consistent design for errors, warnings, successes etc.

![](https://raw.githubusercontent.com/vajahath/lme/master/media/obj-img.png)
![](https://raw.githubusercontent.com/vajahath/lme/master/media/str-img.png)
![](https://raw.githubusercontent.com/vajahath/lme/master/media/lines.png)


## Install

```bash
npm install --save lme
```

## Usage

### Syntax

`lme.<status>(message);`

### Example
```javascript
const lme = require('lme');

lme.d("my kitty is pinky!"); // default style, used for anonymous outputs.
lme.e("Snap! something went wrong."); // used for logging errors.
lme.s("Oh yeah!"); // used for logging success.
lme.w("Attention! Thank you for your attention."); // used for logging warnings.

lme.line() // used to draw lines
lme.eline() // used to draw lines in error theme.
lme.sline() // used to draw lines in success theme.
```

# APIs

**Syntax :** `lme.<status>(message);`

- **where `<status>` can have the following values:**

| status        | name       | when to use                | example               |
| ------------- | ---------- | -------------------------- | --------------------- |
| `d`           | default    | default output             | `lme.d("hi");`        |
| `s`           | success    | on success output          | `lme.s("hi");`        |
| `e`           | error      | on error-ed output         | `lme.e("hi");`        |
| `w`           | warning    | for warnings like output   | `lme.w("hi");`        |
| `h`           | highlight  | for highlighting an output | `lme.h("hi");`        |

<br>

**where `message` can be `string` / `float` / `int` / `objects`.** *(note that javascript treats `arrays` as `objects`.)*

## Drawing lines with `lme.line()`

**Syntax :** `lme.line(character, length)`.

You can prefix `d`, `s`, `e`, `w`, `h` to the `line()` function to obtain the corresponding color scheme for your line. You can also simply use `lme.line()` which has some default values as described below.

### Argument List

| argument        | type       | purpose                                                     | default value    |
| --------------- | ---------- | ----------------------------------------------------------- | ---------------- |
| `character`     | `string`   | determines which character should be used for drawing lines | `-`              |
| `length`        | `integer`  | length of the line                                          | 30               |

<br>

### Examples

```javascript
lme.line();
lme.eline("^");
lme.sline("@", 12);
lme.wline("#", 50);
```

### APIs for drawing lines

| status            | name            | when to use                | example               |
| ----------------- | --------------- | -------------------------- | --------------------- |
| `line`            | default         | default output             | `lme.line();`         |
| `dline`           | same as line    | default output             | `lme.d("hi");`        |
| `sline`           | successe        | on success output          | `lme.s("hi");`        |
| `eline`           | error           | on error-ed output         | `lme.e("hi");`        |
| `wline`           | warning         | for warnings like output   | `lme.w("hi");`        |
| `hline`           | highlight       | for highlighting an output | `lme.h("hi");`        |

<br>
<br>

More configurations are on its way.<br>

If you wish to file any feature/bugs, mention it on [issues](https://github.com/vajahath/lme/issues).

<br>

Enjoy.

## License
MIT &copy; [Vajahath Ahmed](https://mycolorpad.blogspot.in)