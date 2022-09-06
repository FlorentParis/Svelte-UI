<script>
    let bgc = "#5b59d9";
    let textColor = "#ffffff";
    let height = "28px";
  </script>
  
  <div id="compo-container">
    <div id="preview">
      
    </div>
    <div id="code-sources">
      <h2>Html</h2>
      <p>
        &lt;button style="border: none; background-color: {bgc}; color: {textColor};
        font-size: ; border-radius: ; padding: 4px 15px"&gt; 
        &lt;/button&gt;
      </p>
      <h2>Svelte</h2>
      <p>
        &lt;button&gt;  &lt;/button&gt; <br /><br />
        &lt;style&gt; <br /> button &#123; <br />&#160; border: none; <br />&#160;
        background-color: {bgc}; <br />&#160; color: {textColor}; <br />&#160;
        font-size: ;
        <br />&#160; border-radius: ; <br />&#160; padding: 4px 15px
        <br />
        &#125;
        <br />&lt;/style&gt;
      </p>
    </div>
  </div>
  <div id="preferencies">
    
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