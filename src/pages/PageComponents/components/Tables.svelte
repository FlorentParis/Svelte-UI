<script>

let colorThead = '#ff3e00';
let colorTextThead = '#ffffff';
let colorFirstRow = "#000000"
let backgroundColorFirstRow = "#ffffff";
let colorHoverFirstRow = "#ff7f50"
let colorSecondRow = "#000000"
let backgroundColorSecondRow = "#dedede";
let colorHoverSecondRow = "#B55721"
let rowSize = "8px";
let borderSizeTopDown = "1px"
let borderSizeLeftRight = "1px"
let borderColor = "#000000"
let borderColorCSS = borderColor


let borderAppear = "false";


$: if (borderAppear == "true") {
      borderColorCSS = "transparent"
  }else{
      borderColorCSS = borderColor
  }

</script>
  
  <div id="compo-container">
    <div id="preview">
      <div style="width: 90%;">
        <table style=" border-collapse: collapse;
        min-width: 100%; 
        --colorFirstRow:{colorFirstRow};
        --backgroundColorFirstRow:{backgroundColorFirstRow};
        --colorHoverFirstRow:{colorHoverFirstRow};
        --colorSecondRow:{colorSecondRow};
        --backgroundColorSecondRow:{backgroundColorSecondRow};
        --colorHoverSecondRow:{colorHoverSecondRow};
        --rowSize:{rowSize};
        --borderSizeTopDown:{borderSizeTopDown};
        --borderSizeLeftRight: {borderSizeLeftRight};
        --borderColor:{borderColor};
        --borderColorCSS:{borderColorCSS};
        --borderAppear:{borderAppear}">
          <thead>
            <tr style="--thead-color: {colorThead}; --colorTextThead: {colorTextThead}">
              <th>Company</th>
              <th>Contact</th>
              <th>Country</th>
            </tr>
          </thead>
          <tr>
            <td>Alfreds Futterkiste</td>
            <td>Maria Anders</td>
            <td>Germany</td>
          </tr>
          <tr>
            <td>Centro comercial Moctezuma</td>
            <td>Francisco Chang</td>
            <td>Mexico</td>
          </tr>
          <tr>
            <td>Ernst Handel</td>
            <td>Roland Mendel</td>
            <td>Austria</td>
          </tr>
          <tr>
            <td>Island Trading</td>
            <td>Helen Bennett</td>
            <td>UK</td>
          </tr>
        </table>
      </div>
    </div>
    <div id="code-sources">
      <h2>Code Source</h2>
      <p style="word-break: break-word">
        <br />&#160    &lt;div id="compo-container"&gt;
        <br />&#160&#160 &lt;div id="preview"&gt;
        <br />&#160&#160&#160  &lt;div style="width: 90%;"&gt;
        <br />&#160&#160&#160&#160    &lt;table style=" border-collapse: collapse;
                  min-width: 100%; 
                  --colorFirstRow:{colorFirstRow};
                  --backgroundColorFirstRow:{backgroundColorFirstRow};
                  --colorHoverFirstRow:{colorHoverFirstRow};
                  --colorSecondRow:{colorSecondRow};
                  --backgroundColorSecondRow:{backgroundColorSecondRow};
                  --colorHoverSecondRow:{colorHoverSecondRow};
                  --rowSize:{rowSize};
                  --borderSizeTopDown:{borderSizeTopDown};
                  --borderSizeLeftRight: {borderSizeLeftRight};
                  --borderColor:{borderColor};
                  --borderColorCSS:{borderColorCSS};
                  --borderAppear:{borderAppear}"&gt;
        <br />&#160&#160&#160&#160            &lt;thead&gt;
        <br />&#160&#160&#160&#160&#160            &lt;tr style="--thead-color: {colorThead}; --colorTextThead: {colorTextThead}"&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;th&gt;Company&lt;/th&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;th&gt;Contact&lt;/th&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;th&gt;Country&lt;/th&gt;
        <br />&#160&#160&#160&#160&#160        &lt;/tr&gt;
        <br />&#160&#160&#160&#160      &lt;/thead&gt;
        <br />&#160&#160&#160&#160&#160      &lt;tr&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Alfreds Futterkiste&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Maria Anders&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Germany&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160      &lt;/tr&gt;
        <br />&#160&#160&#160&#160&#160        &lt;/tr&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Centro comercial Moctezuma&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Francisco Chang&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Mexico&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160      &lt;/tr&gt;
        <br />&#160&#160&#160&#160&#160        &lt;/tr&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Ernst Handel&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Roland Mendel&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Austria&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160      &lt;/tr&gt;
        <br />&#160&#160&#160&#160&#160      &lt;/tr&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Island Trading&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;Helen Bennett&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160&#160         &lt;td&gt;UK&lt;/td&gt;
        <br />&#160&#160&#160&#160&#160      &lt;/tr&gt;
        <br />&#160&#160&#160&#160    &lt;/table&gt;
        <br />&#160&#160&#160  &lt;/div&gt;
        <br />&#160&#160&lt;/div&gt;
        <br />
        <br />
        <br />
        <br />&#160&#160&lt;style&gt;
        <br />&#160&#160&#160  th:last-child &#123;
        <br />&#160&#160&#160&#160    border: 0;
        <br />&#160&#160&#160  &#125;
        <br />
        <br />&#160&#160&#160  table, td, th &#123;
        <br />&#160&#160&#160&#160    border-top: {borderSizeTopDown} solid;
        <br />&#160&#160&#160&#160    border-bottom: {borderSizeTopDown} solid;
        <br />&#160&#160&#160&#160    border-left: {borderSizeLeftRight} solid;
        <br />&#160&#160&#160&#160    border-right: {borderSizeLeftRight} solid;
        <br />&#160&#160&#160&#160    border-color: {borderColorCSS};
        <br />&#160&#160&#160  &#125;
        <br />
        <br />&#160&#160&#160  table &#123;
        <br />&#160&#160&#160&#160    border-collapse: collapse;
        <br />&#160&#160&#160  &#125;
        <br />
        <br />&#160&#160&#160  th, td &#123;
        <br />&#160&#160&#160&#160    text-align: left;
        <br />&#160&#160&#160&#160    padding: {rowSize};
        <br />&#160&#160&#160  &#125;
        <br />
        <br />&#160&#160&#160  tr:hover &#123;
        <br />&#160&#160&#160&#160 background-color: {colorHoverFirstRow};
        <br />&#160&#160&#160 &#125;
        <br />
        <br />&#160&#160&#160  tr:nth-child(even):hover &#123;
        <br />&#160&#160&#160&#160 background-color: {colorHoverSecondRow};
        <br />&#160&#160&#160&#125;
        <br />
        <br />&#160&#160&#160  th &#123;
        <br />&#160&#160&#160&#160    color: {colorTextThead};
        <br />&#160&#160&#160  &#125;

        <br />&#160&#160&#160  tr&#123;
        <br />&#160&#160&#160&#160    color: {colorSecondRow};
        <br />&#160&#160&#160&#160    background-color: {backgroundColorSecondRow};
        <br />&#160&#160&#160  &#125;

        <br />&#160&#160&#160  tr:nth-child(even)&#123;
        <br />&#160&#160&#160&#160    color: {colorFirstRow};
        <br />&#160&#160&#160&#160    background-color: {backgroundColorFirstRow};
        <br />&#160&#160&#160  &#125;
        <br />&lt;/style&gt;
      </p>
    </div>
  </div>
  <div id="preferencies">
    <div>
      <label for="">Thead Color</label>
      <input
        type="color" 
        bind:value={colorThead}
      />
    </div>
    <div>
      <label for="">Thead Text Color</label>
      <input
        type="color" 
        bind:value={colorTextThead}
      />
    </div>
    <div>
      <label for="">First Row Text Color</label>
      <input
        type="color" 
        bind:value={colorFirstRow}
      />
    </div>
    <div>
      <label for="">First Row Background Color</label>
      <input
        type="color" 
        bind:value={backgroundColorFirstRow}
      />
    </div>
    <div>
      <label for="">First Row Hover Color</label>
      <input
        type="color" 
        bind:value={colorHoverFirstRow}
      />
    </div>
    <div>
      <label for="">Second Row Text Color</label>
      <input
        type="color" 
        bind:value={colorSecondRow}
      />
    </div>
    <div>
      <label for="">Second Row Background Color</label>
      <input
        type="color" 
        bind:value={backgroundColorSecondRow}
      />
    </div>
    <div>
      <label for="">Second Row Hover Color</label>
      <input
        type="color" 
        bind:value={colorHoverSecondRow}
      />
    </div>
    <div>
      <label for="">Row Size</label>
      <select value={rowSize} on:input={(e) => (rowSize = e.target.value)}>
        <option value="8px">xs</option>
        <option value="12px">sm</option>
        <option value="20px">md</option>
        <option value="28px">lg</option>
        <option value="36px">xl</option>
      </select>
    </div>
    <div>
      <label for="">Border Top Down Size</label>
      <select value={borderSizeTopDown} on:input={(e) => (borderSizeTopDown = e.target.value)}>
        <option value="1px">xs</option>
        <option value="2px">sm</option>
        <option value="4px">md</option>
        <option value="8px">lg</option>
        <option value="16px">xl</option>
      </select>
    </div>
    <div>
      <label for="">Border Left Right Size</label>
      <select value={borderSizeLeftRight} on:input={(e) => (borderSizeLeftRight = e.target.value)}>
        <option value="1px">xs</option>
        <option value="2px">sm</option>
        <option value="4px">md</option>
        <option value="8px">lg</option>
        <option value="16px">xl</option>
      </select>
    </div>
    <div>
      <label for="">Border Color</label>
      <input
        type="color" 
        bind:value={borderColor}
      />
    </div>
    <div>
      <label for="">Border Transparent</label>
      <select value={borderAppear} on:input={(e) => (borderAppear = e.target.value)}>
        <option value="true">Yes</option>
        <option value="false">No</option>
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
      overflow: scroll;
      max-height: 500px;
    }
  
    #preferencies {
      display: flex;
      gap: 30px;
      padding: 20px 90px;
      justify-content: center;
    }

    th:last-child {
      border: 0;
    }

    table, td, th {
      border-top: var(--borderSizeTopDown) solid;
      border-bottom: var(--borderSizeTopDown) solid;
      border-left: var(--borderSizeLeftRight) solid;
      border-right: var(--borderSizeLeftRight) solid;
      border-color: var(--borderColorCSS);
    }

    table {
      border-collapse: collapse;
    }

    th, td {
      text-align: left;
      padding: var(--rowSize);
    }

    tr:hover {background-color: var(--colorHoverFirstRow);}

    tr:nth-child(even):hover {background-color: var(--colorHoverSecondRow);}

    th {
      background-color: var(--thead-color);
      color: var(--colorTextThead);
    }

    tr{
      color: var(--colorSecondRow);
      background-color: var(--backgroundColorSecondRow);
    }

    tr:nth-child(even){
      color: var(--colorFirstRow);
      background-color: var(--backgroundColorFirstRow);
    }
    
  
  </style>  