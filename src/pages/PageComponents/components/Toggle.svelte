<script>
    let btn = "#000000";
    let btnCheck = "#ffffff";
    let bgc = "#ffffff";
    let bgcCheck = "#000000";
    let textValue = "Text";
    let size = "28px";
</script>

<div id="compo-container" style="--bgc: {bgc}; --bgcCheck: {bgcCheck}; --btn: {btn}; --btnCheck: {btnCheck}">
  <div id="preview">
    <div>
      <input type="checkbox" id="toggle"/>
      <label for="toggle" id="toggle_label"></label>
    </div>
  </div>
  <div id="code-sources">
    <h2>Html</h2>
    <p>
      &lt;div style="border: none; background-color: {bgc}; color: {bgcCheck};
      font-size: {size}; border-radius: 100px; padding: 4px 15px"&gt; {textValue}
      &lt;/div&gt;
    </p>
    <h2>Svelte</h2>
    <p>
      &lt;button&gt; {textValue} &lt;/button&gt; <br /><br />
      &lt;style&gt; <br /> button &#123; <br />&#160; border: none; <br />&#160;
      background-color: {bgc}; <br />&#160; color: {bgcCheck}; <br />&#160;
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
        <label for="">Btn Color</label>
        <input type="color" value={btn} on:input={(e) => btn = e.target.value} />
    </div>
  <div>
    <label for="">Btn Color Check</label>
    <input type="color" value={btnCheck} on:input={(e) => btnCheck = e.target.value} />
  </div>

  <div>
    <label for="">bgc Color</label>
    <input
      type="color"
      value={bgc}
      on:input={(e) => bgc = e.target.value}
    />
  </div>
  <div>
    <label for="">bgc Color Check</label>
    <input
      type="color"
      value={bgcCheck}
      on:input={(e) => bgcCheck = e.target.value}
    />
  </div>

  <div>
    <label for="">Size</label>
    <select value={size} on:input={(e) => size = e.target.value}>
      <option value="12px">sm</option>
      <option value="20px">md</option>
      <option value="28px">lg</option>
      <option value="36px">xl</option>
    </select>
  </div>
</div>

<style>
    #toggle {
        visibility: hidden; 
    }

    #toggle:checked + label {
        background-color: var(--bgcCheck); /* couleur du background check */
    }

    #toggle + label:before {
        transition: all .75s ease;
    }

    #toggle:checked + label:before {
        transform: translateX(95px);
        background-color: var(--btnCheck); /* couleur du boutton check */
    }

    #toggle_label {
        transition: background-color .75s ease;
        display: flex;
        width: 180px;
        height: 90px;
        border: 6px solid;
        border-radius: 99em;
        position: relative;
        cursor: pointer;
        background-color: var(--bgc)
    }

    #toggle_label:before {
        transition: transform .75s ease;
        content: "";
        position: absolute;
        width: 54px;
        height: 54px;
        background-color: var(--btn); /* couleur du boutton*/
        border-radius: 50%;
        top: 17px;
        left: 17px;
    }

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