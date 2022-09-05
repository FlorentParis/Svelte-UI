<script>
  let bgc = "#5b59d9";
  let textColor = "#ffffff";
  let textValue = "Text";
  let size = "28px";
  let borderRadius = "2px";
</script>

<div id="compo-container">
  <div id="preview">
    <button
      style="background-color: {bgc}; color: {textColor}; font-size: {size}; border-radius: {borderRadius}; padding: 4px 15px"
    >
      {textValue}
    </button>
  </div>
  <div id="code-sources">
    <p>
      &lt;button style="border: none; background-color: {bgc}; color: {textColor};
      font-size: {size}; border-radius: {borderRadius}; padding: 4px 15px"&gt; {textValue}
      &lt;/button&gt;
    </p>
  </div>
</div>
<div id="preferencies">
  <div>
    <label for="">Background Color</label>
    <input type="color" value={bgc} on:input={(e) => (bgc = e.target.value)} />
  </div>

  <div>
    <label for="">Text Color</label>
    <input
      type="color"
      value={textColor}
      on:input={(e) => (textColor = e.target.value)}
    />
  </div>

  <div>
    <label for="">Text</label>
    <input
      type="text"
      value={textValue}
      on:input={(e) => (textValue = e.target.value)}
    />
  </div>

  <div>
    <label for="">Size</label>
    <select value={size} on:input={(e) => (size = e.target.value)}>
      <option value="12px">sm</option>
      <option value="20px">md</option>
      <option value="28px">lg</option>
      <option value="36px">xl</option>
    </select>
  </div>

  <div>
    <label for="">Border Radius</label>
    <select
      value={borderRadius}
      on:input={(e) => (borderRadius = e.target.value)}
    >
      <option value="0px">0</option>
      <option value="2px">1</option>
      <option value="10px">2</option>
      <option value="15px">3</option>
      <option value="20px">4</option>
      <option value="30px">5</option>
    </select>
  </div>
</div>

<style>
  #compo-container {
    padding: 20px 90px;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  #preview {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  #code-sources {
    background-color: rgba(208, 208, 208, 0.341);
    border-radius: 5px;
    min-height: 300px;
    padding: 0 20px;
  }

  #preferencies {
    display: flex;
    gap: 30px;
    padding: 20px 90px;
    justify-content: center;
  }

  button {
    border: none;
  }
</style>
