# grid-gallery-react
```
<!DOCTYPE html>
<html>
<head>
<style>
.grid-container {
  display: grid;
  width: 100vw;
  margin-left: calc(-50vw + 50%);
  grid-template-columns: repeat(12, 1fr);
  grid-auto-rows: 8.333vw;
  gap: 2px;
  grid-auto-flow: dense;
  background-color: #2196F3;
}

.grid-container > div {

	position: relative;
  	background-color: rgba(255, 255, 255, 0.8);
}

  .large {
      grid-area: span 4 / span 4;
    }
  .medium {
    grid-area: span 2 / span 2;
  }
  .small {
    grid-area: span 1 / span 1;
  }
  .half {
    grid-area: span 2 / span 6;
  }
</style>
</head>
<body>

<h1>The grid-area Property</h1>

<p>You can use the <em>grid-area</em> property to specify where to place an item.</p>
<p>The syntax is grid-row-start / grid-column-start / grid-row-end / grid-column-end.</p>
<p>Item1 will start on row 2 and column 1, and span 2 rows and 3 columns:</p>

<div class="grid-container">
  <div class="large">1</div>  <div class="large">1</div>
  <div class="large">1</div>
    <div class="medium">2</div>

  <div class="large">1</div>
  <div class="large">1</div>
  <div class="large">1</div>

  <div class="medium">2</div>  <div class="medium">2</div>
  <div class="medium">2</div>
  <div class="medium">2</div>

  <div class="medium">3</div>  
  <div class="small">4</div>
  <div class="small">5</div>  <div class="small">5</div>
  <div class="small">5</div>
  <div class="small">5</div>
  <div class="small">5</div>
  <div class="small">5</div>

  <div class="large">6</div>
  <div class="medium">7</div>
</div>

</body>
</html>
```

# media

```
  ${media.medium(css`
    .large {
      grid-area: span 6 / span 6;
    }
    .medium {
      grid-area: span 4 / span 4;
    }
    .small {
      grid-area: span 2 / span 2;
    }
    .half {
      grid-area: span 2 / span 6;
    }
  `)}

  ${media.small(css`
    .large {
      grid-area: span 8 / span 8;
    }
    .medium {
      grid-area: span 4 / span 4;
    }
    .small {
      grid-area: span 2 / span 2;
    }
    .half {
      grid-area: span 2 / span 12;
    }
  `)}
```

![Image alt](https://i.imgur.com/k6E745l.png)
