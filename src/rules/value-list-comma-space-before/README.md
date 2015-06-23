# value-list-comma-space-before

Require or disallow a single space before the commas of value lists.

```css
    a { background-size: 0, 0; }
/**                       ↑  
 * The space before these commas */
```

## Options

`string`: `"always"|"never"|"always-single-line"|"never-single-line"`

### `"always"`

There *must always* be a single space before the comma.

The following patterns are considered warnings:

```css
a { background-size: 0,0; }
```

```css
a { background-size: 0
      , 0; }
```

The following patterns are *not* considered warnings:

```css
a { background-size: 0 ,0; }
```

```css
a { background-size: 0 ,
      0; }
```

### `"never"`

There *must never* be whitespace before the comma.

The following patterns are considered warnings:

```css
a { background-size: 0 ,0; }
```

```css
a { background-size: 0 ,
      0; }
```

The following patterns are *not* considered warnings:

```css
a { background-size: 0,0; }
```

```css
a { background-size: 0, 
      0; }
```

### `"always-single-line"`

There *must always* be a single space before the comma in single-line value lists.

The following patterns are considered warnings:

```css
a { background-size: 0,0; }
```

The following patterns are *not* considered warnings:

```css
a { background-size: 0 ,0; }
```

```css
a { background-size: 0 ,
      0; }
```

```css
a { background-size: 0
      , 0; }
```

### `"never-single-line"`

There *must never* be whitespace before the comma in single-line value lists.

The following patterns are considered warnings:

```css
a { background-size: 0 ,0; }
```

The following patterns are *not* considered warnings:

```css
a { background-size: 0,0; }
```

```css
a { background-size: 0, 
      0; }
```

```css
a { background-size: 0 ,
      0; }
```