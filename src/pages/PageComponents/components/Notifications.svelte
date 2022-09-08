<script>
    let bgc = "#5b59d9";
    
    let title = "Caution !";
    let text = "Holala dangerous data !";
    let titleColor = "#000000";
    let textColor = "#000000";
    let shadow = "rgba(0, 0, 0, 0.24) 0px 3px 8px";
    let radius = "5px";
  </script>
  
  <div id="compo-container">
    <div id="preview">
      <div id="notif" style="box-shadow: {shadow}; border-radius: {radius};">
        <img src="http://cdn.onlinewebfonts.com/svg/img_29386.png" alt="">
        <div>
          <span style="color: {titleColor};">{title}</span>
          <p style="color: {textColor};">{text}</p>
        </div>
        <span id="cross">X</span>
      </div>
    </div>
    <div id="code-sources">
      <h2>Code Sources</h2>
      <p>
        &lt;div id="notif"&gt; <br />
          &#160;&lt;img src="http://cdn.onlinewebfonts.com/svg/img_29386.png" alt=""/&gt; <br/>
          &#160;&lt;div&gt; <br />
            &#160; &lt;span&gt;{title}&lt;/span&gt; <br />
            &#160; &lt;p&gt;{text}&lt;/p&gt; <br />
          &#160;&lt;/div&gt; <br />
          &#160; &lt;span id="cross"&gt;X&lt;/span&gt; <br />
        &lt;/div&gt; <br /><br />

        &lt;style&gt; <br /> #notif &#123; <br />&#160; width: 260px; <br />&#160;
        height: 80px; <br />&#160; display: flex; <br />&#160;
        align-items: center;
        <br />&#160; border-radius: {radius}; <br />&#160; padding: 0 15px;
        <br />&#160; position: relative; <br /> &#160; gap: 15px; <br /> &#160; box-shadow: {shadow}; <br />
        &#125;
        
        <br />
        #notif img &#123; <br />&#160; height: 70%; <br />
        &#125;
        
        <br />
        #notif > div &#123; <br />&#160; display: flex; <br />&#160;
        flex-direction: column; <br />&#160; gap: 5px; <br />
        &#125;
        
        <br />
        #notif > div > span &#123; <br />&#160; font-weight: 700; <br /> &#160; color: {titleColor}; <br />
        &#125;
        
        <br />
        #notif p &#123; <br />&#160; margin: 0; <br /> &#160; color: {textColor}; <br />
        &#125;
        
        <br />
        #notif #cross &#123; <br />&#160; position: absolute; <br />&#160;
        top: 10px; <br />&#160; right: 10px; <br />
        &#125;
        <br />&lt;/style&gt;
      </p>
    </div>
  </div>
  <div id="preferencies">
    <div>
      <label for="">Title</label>
      <input
        type="text"
        value={title}
        on:input={(e) => (title = e.target.value)}
      />
    </div>

    <div>
      <label for="">Text</label>
      <input
        type="text"
        value={text}
        on:input={(e) => (text = e.target.value)}
      />
    </div>

    <div>
      <label for="">Title Color</label>
      <input
        type="color"
        value={titleColor}
        on:input={(e) => (titleColor = e.target.value)}
      />
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
      <label for="">Shadow</label>
      <select value={shadow} on:input={(e) => (shadow = e.target.value)}>
        <option value="rgba(149, 157, 165, 0.2) 0px 8px 24px">0</option>
        <option value="rgba(100, 100, 111, 0.2) 0px 7px 29px 0px">1</option>
        <option value="rgba(0, 0, 0, 0.24) 0px 3px 8px">2</option>
        <option value="rgba(0, 0, 0, 0.02) 0px 1px 3px 0px, rgba(27, 31, 35, 0.15) 0px 0px 0px 1px">3</option>
      </select>
    </div>

    <div>
      <label for="">Border Radius</label>
      <select value={radius} on:input={(e) => (radius = e.target.value)}>
        <option value="0px">0</option>
        <option value="5px">1</option>
        <option value="10px">2</option>
        <option value="15px">3</option>
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
      max-height: 500px;
      overflow-y: scroll;
      overflow-wrap: break-word;
    }
  
    #preferencies {
      display: flex;
      gap: 30px;
      padding: 20px 90px;
      justify-content: center;
    }
  
    #notif {
      width: 260px;
      height: 80px;
      display: flex;
      align-items: center;
      padding: 0 15px;
      position: relative;
      gap: 15px;
    }

    #notif img {
      height: 70%;
    }

    #notif > div {
      display: flex;
      flex-direction: column;
      gap: 5px;
    }

    #notif > div > span {
      font-weight: 700;
    }

    #notif p {
      margin: 0;
    }

    #notif #cross {
      position: absolute;
      top: 10px;
      right: 10px;
    }
  </style>  