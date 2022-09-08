<script>
    let bgc = "#5b59d9";
    let textColor = "#ffffff";
    let navHeight = "140px";
    let imgHeight = "70%";
    let fontSize = "18px";
    let fontFamily = "sans-serif";
  </script>
  
  <div id="compo-container">
    <div id="preview">
      <nav style="background-color: {bgc}; height: {navHeight};">
        <div>
            <img src="https://upload.wikimedia.org/wikipedia/commons/a/ab/Android_O_Preview_Logo.png" alt="Logo" style="height: {imgHeight};">
            <ul style="font-size: {fontSize}; font-family: {fontFamily};">
                <li>
                    <a href="Page1" style="color: {textColor};">Lien 1</a>
                </li>
                <li>
                    <a href="Page2" style="color: {textColor};">Lien 2</a>
                </li>
                <li>
                    <a href="Page3" style="color: {textColor};">Lien 3</a>
                </li>
            </ul>
        </div>
      </nav>
    </div>
    <div id="code-sources">
        <h2>Code Sources</h2>
      <p>
        &lt;nav&gt; <br />
        &#160; &lt;div&gt; <br />
        &#160; &#160; &lt;img src="https://upload.wikimedia.org/wikipedia/commons/a/ab/Android_O_Preview_Logo.png" alt="Logo"&gt; <br />
        &#160; &#160; &lt;ul&gt; <br />
        &#160; &#160; &#160; &lt;li&gt; &lt;a href="Page1"&gt;Lien 1&lt;/a&gt; &lt;/li&gt; <br />
        &#160; &#160; &#160; &lt;li&gt; &lt;a href="Page2"&gt;Lien 2&lt;/a&gt; &lt;/li&gt; <br />
        &#160; &#160; &#160; &lt;li&gt; &lt;a href="Page3"&gt;Lien 3&lt;/a&gt; &lt;/li&gt; <br />
        &#160; &#160; &lt;ul&gt; <br />
        &#160; &#160; &lt;img&gt; <br />
        &#160; &lt;div&gt; <br />
        &lt;nav&gt; <br />
        <br />
        &lt;style&gt; <br /> 
        &#160; nav &#123; <br />
        &#160; &#160; border: none; <br />
        &#160; &#160; display: flex; <br />
        &#160; &#160; justify-content: center; <br />
        &#160; &#160; align-items: center; <br />
        &#160; &#160; background-color: {bgc}; <br />
        &#160; &#160; height: {navHeight}; <br />
        &#160; &#160; width: 100%; <br />
        &#160; &#125; <br />
        <br />
        &#160; nav > div &#123; <br />
        &#160; &#160; display: flex; <br />
        &#160; &#160; justify-content: space-between; <br />
        &#160; &#160; align-items: center; <br />
        &#160; &#160; height: 100%; <br />
        &#160; &#160; width: 100%; <br />
        &#160; &#160; max-width: 1920px; <br />
        &#160; &#160; padding: 0 40px; <br />
        &#160; &#125; <br />
        <br />
        &#160; nav img &#123; <br />
        &#160; &#160; height: {imgHeight}; <br />
        &#160; &#125; <br />
        <br />
        &#160; nav ul &#123; <br />
        &#160; &#160; display: flex; <br />
        &#160; &#160; list-style: none; <br />
        &#160; &#160; gap: 40px; <br />
        &#160; &#160; font-size: {fontSize}; <br />
        &#160; &#160; font-family: {fontFamily}; <br />
        &#160; &#125; <br />
        <br />
        &#160; nav a &#123; <br />
        &#160; &#160; color: {textColor}; <br />
        &#160; &#125; <br />
        <br />

        <br />&lt;/style&gt;
      </p>
    </div>
  </div>
  <div id="preferencies">
    <div>
        <label for="">Background Color</label>
        <input type="color" value={bgc} on:input={(e) => bgc = e.target.value} />
    </div>
    <div>
        <label for="">Text Color</label>
        <input type="color" value={textColor} on:input={(e) => textColor = e.target.value} />
    </div>
    <div>
        <label for="">Nav Height</label>
        <select name="" value={navHeight} on:input={(e) => navHeight = e.target.value}>
            <option value="60px">Small</option>
            <option value="100px">Medium</option>
            <option value="140px">Large</option>
            <option value="200px">Extra Large</option>
        </select>
    </div>
    <div>
        <label for="">Img Height</label>
        <select name="" value={imgHeight} on:input={(e) => imgHeight = e.target.value}>
            <option value="50%">Small</option>
            <option value="70%">Medium</option>
            <option value="90%">Large</option>
            <option value="100%">Extra Large</option>
        </select>
    </div>
    <div>
        <label for="">Font Size</label>
        <select name="" value={fontSize} on:input={(e) => fontSize = e.target.value}>
            <option value="16px">Small</option>
            <option value="18px">Medium</option>
            <option value="20px">Large</option>
            <option value="24px">Extra Large</option>
        </select>
    </div>
    <div>
        <label for="">Font Family</label>
        <select name="" value={fontFamily} on:input={(e) => fontFamily = e.target.value}>
            <option value="sans-serif">Sans Serif</option>
            <option value="Roboto">Roboto</option>
            <option value="Bebas Neue">Bebas Neue</option>
            <option value="EB Garamond">EB Garamond</option>
        </select>
    </div>
  </div>
  
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=EB+Garamond&display=swap');

    #compo-container {
      padding: 20px 90px;
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
  
    #preview {
      display: flex;
      align-items: center;
      justify-content: center;
      padding-right: 60px;
    }
  
    #code-sources {
      background-color: rgba(208, 208, 208, 0.341);
      border-radius: 5px;
      min-height: 300px;
      padding: 0 20px;
      max-height: 500px;
      overflow-y: scroll;
    }
  
    #preferencies {
      display: flex;
      gap: 30px;
      padding: 20px 90px;
      justify-content: center;
    }

    nav {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
    }

    nav > div {
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 100%;
        width: 100%;
        max-width: 1920px;
        padding: 0 40px;
    }

    nav ul {
        display: flex;
        list-style: none;
        gap: 40px;
    }
  
  </style>  