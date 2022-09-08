<script>
  let bgc = "#e84545";
  let textColor = "#ffffff";
  let textValue = "Text";
  let size = "28px";
</script>

<div id="compo-container">
  <div id="preview">
    <div
      style="background-color: {bgc}; color: {textColor}; font-size: {size}; border-radius: 100px; padding: 4px 15px"
    >
      {textValue}
    </div>
  </div>
  <div id="code-sources">
    <h2>Code Sources</h2>
    <p>
      &lt;button&gt; {textValue} &lt;/button&gt; <br /><br />
      &lt;style&gt; <br /> button &#123; <br />&#160; border: none; <br />&#160;
      background-color: {bgc}; <br />&#160; color: {textColor}; <br />&#160;
      font-size: {size};
      <br />&#160; border-radius: 100px; <br />&#160; padding: 4px 15px
      <br />
      &#125;
      <br />&lt;/style&gt;
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
</style>
