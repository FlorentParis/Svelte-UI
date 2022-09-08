<script>
    let btn = "#000000";
    let btnCheck = "#ffffff";
    let bgc = "#ffffff";
    let bgcCheck = "#000000";
    let textValue = "Text";
    let size = 4;
</script>

<div id="compo-container" style="--bgc: {bgc}; --bgcCheck: {bgcCheck}; --btn: {btn}; --btnCheck: {btnCheck}; --size: {size}">
  <div id="preview">
    <div>
      <input type="checkbox" id="toggle"/>
      <label for="toggle" id="toggle_label"></label>
    </div>
  </div>
  <div id="code-sources">
    <h2>Html</h2>
    <p>
      &lt;input type="checkbox"&gt<br />
      &lt;label for="toggle" &lt;/label&gt;
    </p>
    <h2>Svelte</h2>
    <p>
      &lt;input type="checkbox" id="toggle"&gt; <br />
      &lt;label for="toggle" id="toggle_label"&gt; &lt;/label&gt;
      <br /><br />
      &lt;style&gt; <br /> 
      #toggle &#123; <br />&#160; visibility: hidden;<br />&#125;<br />
      #toggle:checked + label &#123; <br />&#160; background-color: {bgcCheck};<br />&#125;<br />
      #toggle + label:before &#123; <br />&#160; transition: all .75s ease;<br />&#125;<br />
      #toggle:checked + label:before &#123; <br />&#160; transform: translateX({95/size}px);<br />&#160; background-color: {btnCheck};<br /> &#125;<br />
      #toggle_label &#123; <br />&#160; transition: all .75s ease;<br />&#160; display: flex;<br />&#160; width: {180/size}px;<br />&#160; height: {90/size}px;<br />&#160; border: {6/size}px solid;<br />&#160; border-radius: 99em;<br />&#160; position: relative;<br />&#160; cursor: pointer;<br />&#160; background-color: {bgc}<br />&#125;<br />
      #toggle_label:before &#123; <br />&#160; transition: transform .75s ease;<br />&#160; content: "";<br />&#160; position: absolute;<br />&#160; width: {54/size}px;<br />&#160; height: {54/size}px;<br />&#160; background-color: {btn};<br />&#160; border-radius: 50%;<br />&#160; top: {17/size}px;<br />&#160; left: {17/size}px;&#125;<br />
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
    <label for="">bgc</label>
    <input
      type="color"
      value={bgc}
      on:input={(e) => bgc = e.target.value}
    />
  </div>
  <div>
    <label for="">bgc Check</label>
    <input
      type="color"
      value={bgcCheck}
      on:input={(e) => bgcCheck = e.target.value}
    />
  </div>

  <div>
    <label for="">Size</label>
    <select value={size} on:input={(e) => size = e.target.value}>
      <option value=4>sm</option>
      <option value=3>md</option>
      <option value=2>lg</option>
      <option value=1>xl</option>
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
        transform: translateX(calc(95px/var(--size)));
        background-color: var(--btnCheck); /* couleur du boutton check */
    }

    #toggle_label {
        transition: all .75s ease;
        display: flex;
        width: calc(180px/var(--size));
        height: calc(90px/var(--size));
        border: calc(6px/var(--size)) solid;
        border-radius: 99em;
        position: relative;
        cursor: pointer;
        background-color: var(--bgc)
    }

    #toggle_label:before {
        transition: transform .75s ease;
        content: "";
        position: absolute;
        width: calc(54px/var(--size));
        height: calc(54px/var(--size));
        background-color: var(--btn); /* couleur du boutton*/
        border-radius: 50%;
        top: calc(17px/var(--size));
        left: calc(17px/var(--size));
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
        overflow: scroll;
        max-height: 500px;
    }

    #preferencies {
        display: flex;
        gap: 30px;
        padding: 20px 90px;
        justify-content: center;
    }
</style>