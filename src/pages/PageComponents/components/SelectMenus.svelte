<script>
  let bgc = "#ffffff";
  let textColor = "#000000";
  let size = "28px";
  let borderRadius = "2px";
  let border="1px solid";
</script>

<div id="compo-container">
    <div id="preview">
        <label>Mon select</label>
        <select id="select" style="background-color: {bgc}; color: {textColor}; font-size: {size}; border-radius: {borderRadius}; border:{border};">
            <option value="value1">Valeur 1</option>
            <option value="value2">Valeur 2</option>
            <option value="value3">Valeur 3</option>
        </select>
    </div>
    <div id="code-sources">
        <h2>Code Sources</h2>
        <p>
            &lt;label&gt;Mon select&lt;/label&gt; <br />
            &lt;select&gt;<br />&#160;
            &lt;option value="value1"&gt; Value 1 &lt;/option &gt; <br /> &#160;
            &lt;option value="value1"&gt; Value 1 &lt;/option &gt; <br /> &#160;
            &lt;option value="value1"&gt; Value 1 &lt;/option &gt; <br />
            &lt;/select&gt; <br/> <br/>

            &lt;style&gt; <br /> select &#123; <br />&#160; border: {border}; <br />&#160;
            background-color: {bgc}; <br />&#160; color: {textColor}; <br />&#160;
            font-size: {size};
            <br />&#160; border-radius: {borderRadius}; <br />&#160; padding: 4px 15px;
            <br />margin-top: 5px; <br />&#160;width: 200px; <br />&#160;
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

    <div>
        <label for="">Border Style</label>
        <select
                value={border}
                on:input={(e) => (border = e.target.value)}
        >
            <option value="1px solid">Default</option>
            <option value="none">None</option>
            <option value="1px dashed">Dashed</option>
            <option value="1px dotted">Dotted</option>
            <option value="double">Double</option>
            <option value="1px groove">Groove</option>
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
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    #code-sources {
        background-color: rgba(208, 208, 208, 0.341);
        border-radius: 5px;
        max-height: 500px;
        overflow: scroll;
        min-height: 300px;
        padding: 0 20px;
    }

    #preferencies {
        display: flex;
        gap: 30px;
        padding: 20px 90px;
        justify-content: center;
    }

    select{
        margin-top: 5px;
        width: 200px;
    }
</style>
