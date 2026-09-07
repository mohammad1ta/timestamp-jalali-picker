# Timestamp Jalali Picker

`timestamp.js` is a small, free Jalali (Persian) date and time picker. It injects its own styles, so no CSS file or jQuery is required.  
Developed and maintained by [Timestamp](https://timestamp.ir).

## Include it

```html
<script src="timestamp.js"></script>
```

Then create a picker manually:

```html
<input id="published-at" type="text" placeholder="1405-06-11 14:30">
<script>
  Timestamp.setup({
    inputField: 'published-at',
    ifFormat: '%Y-%m-%d %H:%M',
    showsTime: true
  });
</script>
```

## Automatic legacy attributes

Inputs using these attributes are initialized automatically once the page is ready:

```html
<input data-rel="calendar">          <!-- YYYY-MM-DD HH:mm:ss -->
<input data-rel="calendardate">      <!-- YYYY-MM-DD -->
<input data-rel="calendartime">      <!-- HH:mm -->
<input data-rel="calendardatetime">  <!-- YYYY-MM-DD HH:mm -->
```

## Options

| Option | Default | Description |
| --- | --- | --- |
| `inputField` | required | Input element or its `id`. |
| `ifFormat` | `%Y-%m-%d` | Output format. Supports `%Y`, `%y`, `%m`, `%d`, `%H`, `%M`, `%S`, `%B`, `%A`. |
| `showsTime` | `false` | Shows hour and minute controls. Add `%S` to include seconds. |
| `singleClick` | `true` | Closes the picker after choosing a date. |
| `autoShowOnFocus` | `false` | Opens the picker when the input receives focus. |
| `onSelect` | none | Callback called after a value is chosen. |
| `onClose` | none | Callback called when the popup closes. |

For compatibility with existing code, `Calendar.setup({...})` is also available and maps to `Timestamp.setup({...})`.

Open `example.html` directly in a browser to try each built-in mode.
