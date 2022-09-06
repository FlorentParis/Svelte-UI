<script>
    let firstText = "firstText";
    let firstTextColor = "#000000"
    let secondText ="Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    let secondTextColor = "#858b96"
    let firstButtonText = "firstButton";
    let firstButtonColor = "#4f46e5";
    let firstButtonTextColor = "#ffffff";
    let secondButtonColor = "#ffffff";
    let secondButtonTextColor = "#000000"

    let openModal = false;


    function toggleModal() {
        openModal = !openModal
    }
</script>



<div id="compo-container">
    <div id="preview" style="position: relative;background-image:url('https://www.easytutoriel.com/wp-content/uploads/2021/09/fond-d-ecran-anime-windows-11-10-tutoriel-facile.jpg'); background-repeat: no-repeat;background-size: cover;">
        <button id="myBtn" on:click={toggleModal}>Open Modal</button>
        <div style="    width: 100%;
        height: 100%;
        align-items: center;
        position: absolute;
        justify-content: center;
        backdrop-filter: blur(2px);
        display:{openModal?"flex":"none"}">
            <div id="modal" style="border:none; border-radius: 15px; max-width: 500px;     background-color: #ffff;">
                <div style="display:flex; flex-direction: column;    align-items: center; margin: 30px;">
                    <h3 style="color: {firstTextColor}">{firstText}</h3>
                    <p style="color: {secondTextColor};     text-align: center; word-break: break-word;">{secondText}</p>
                    <div style="    width: 100%;
                    display: flex;
                    justify-content: space-around;
                    gap:20px">
                    <button style="background-color:{firstButtonColor}; color: {firstButtonTextColor}; font-size: 20px; border-radius: 20px; padding: 4px 15px; border:none"> {firstButtonText} </button>
                    <button on:click={toggleModal} style="background-color:{secondButtonColor}; color: {secondButtonTextColor}; font-size: 20px; border-radius: 20px; padding: 4px 15px; border-color:#d1d5db"> Cancel </button>
                </div>
            </div>
        </div>
      </div>
    </div>
    <div id="code-sources">
      <h2>Html</h2>
      <p style="word-break: break-word">
        &lt;script&gt;
        <br />    let openModal = false;

        <br />    function toggleModal() &#123;
        <br />  openModal = !openModal
        <br />  &#125;
        <br />&lt;/script&gt;
        <br />&lt;button id="myBtn" on:click=&#123;toggleModal&#125;&gt;Open Modal&lt;/button&gt;
        &lt;div id="preview" style="position: relative;background-image:url('https://www.easytutoriel.com/wp-content/uploads/2021/09/fond-d-ecran-anime-windows-11-10-tutoriel-facile.jpg'); background-repeat: no-repeat;background-size: cover;"&gt;
            &lt;button id="myBtn" on:click=&#123;toggleModal&#125;&gt;Open Modal&lt;/button&gt;
            &lt;div style="    width: 100%;
            height: 100%;
            align-items: center;
            position: absolute;
            justify-content: center;
            backdrop-filter: blur(2px);
            display:{openModal?"flex":"none"}"&gt;
                &lt;div id="modal" style="border:none; border-radius: 15px; max-width: 500px;     background-color: #ffff;"&gt;
                    &lt;div style="display:flex; flex-direction: column;    align-items: center; margin: 30px;"&gt;
                        &lt;h3 style="color: {firstTextColor}"&gt;{firstText}&lt;/h3&gt;
                        &lt;p style="color: {secondTextColor};     text-align: center; word-break: break-word;"&gt;{secondText}&lt;/p&gt;
                        &lt;div style="    width: 100%;
                        display: flex;
                        justify-content: space-around;
                        gap:20px"&gt;
                        &lt;button style="background-color:{firstButtonColor}; color: {firstButtonTextColor}; font-size: 20px; border-radius: 20px; padding: 4px 15px; border:none"&gt; {firstButtonText} &lt;/button&gt;
                        &lt;button on:click=&#123;toggleModal&#125; style="background-color:{secondButtonColor}; color: {secondButtonTextColor}; font-size: 20px; border-radius: 20px; padding: 4px 15px; border-color:#d1d5db"&gt; Cancel &lt;/button&gt;
                    &lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      </p>
      <h2>Svelte</h2>
      <p>
        &lt;script&gt;
        <br />  &#160;  let openModal = false;

        <br />  &#160;  function toggleModal() &#123;
        <br />  &#160;	&#160;	openModal = !openModal
        <br />  &#125;
        <br />&lt;/script&gt;
        <br />&lt;button id="myBtn" on:click=&#123;toggleModal&#125;&gt;Open Modal&lt;/button&gt;
        <br />&lt;div id="preview"&gt;
        <br />    &lt;button id="myBtn" on:click=&#123;toggleModal&#125;&gt;Open Modal&lt;/button&gt;
        <br />    &lt;div id="modal-parent"&gt;
        <br />        &lt;div id="modal"&gt;
        <br />            &lt;div id="modal-content" &gt;
        <br />                &lt;h3 &gt;{firstText}&lt;/h3&gt;
        <br />                &lt;p &gt;{secondText}&lt;/p&gt;
        <br />               &lt;div id="modal-button-container" &gt;
        <br />               &lt;button &gt; {firstButtonText} &lt;/button&gt;
        <br />               &lt;button on:click=&#123;toggleModal&#125;&gt; Cancel &lt;/button&gt;
        <br />           &lt;/div&gt;
        <br />        &lt;/div&gt;
        <br />    &lt;/div&gt;
        <br />  &lt;/div&gt;
        <br />&lt;/div&gt;
        <br />
        <br /> &lt;style&gt;
        <br />  #preview &#123;
        <br />          position: relative;
        <br />          background-image: url(https://www.easytutoriel.com/wp-content/uploads/2021/09/fond-d-ecran-anime-windows-11-10-tutoriel-facile.jpg);
        <br />          background-repeat: no-repeat;
        <br />          background-size: cover;
        <br /> &#125;
        <br /> .modal-parent &#123;
        <br/>     width: 100%;
        <br/>     height: 100%;
        <br/>     align-items: center;
        <br/>     position: absolute;
        <br/>     justify-content: center;
        <br/>     backdrop-filter: blur(2px);
        <br/>     display: {openModal?"flex":"none"};
        <br /> &#125;
        <br /> .modal &#123;
        <br/>       border: none;
        <br/>       border-radius: 15px;
        <br/>       max-width: 500px;
        <br/>       background-color: rgb(255, 255, 255);
        <br /> &#125;
        <br/> .modal-content &#123;
        <br />     display: flex;
        <br />    flex-direction: column;
        <br />    align-items: center;
        <br />    margin: 30px;
        <br /> &#125;
        <br /> h3 &#123;
        <br /> color: {firstTextColor};
        <br /> &#125;
        <br /> p &#123;
        <br />     color: {secondTextColor};
        <br />     text-align: center;
        <br />     word-break: break-word;
        <br /> &#125;
        <br /> .modal-button-container &#123; 
        <br />     width: 100%;
        <br />     display: flex;
        <br />     justify-content: space-around;
        <br />     gap: 20px;
        <br /> &#125;
        <br /> #first-button &#123;
        <br />     background-color: {firstButtonColor};
        <br />     color: {firstButtonTextColor};
        <br />     font-size: 20px;
        <br />     border-radius: 20px;
        <br />     padding: 4px 15px;
        <br />     border: none;
        <br /> &#125;
        <br /> #second-button &#123; 
        <br />     background-color: {secondButtonColor};
        <br />     color: {secondButtonTextColor};
        <br />     font-size: 20px;
        <br />     border-radius: 20px;
        <br />     padding: 4px 15px;
        <br />     border-color: rgb(209, 213, 219);
        <br /> &#125;
        <br /> &lt;/style&gt;
      </p>
    </div>
</div>
<div id="preferencies">
    <div style="display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-column-gap: 0px;
    grid-row-gap: 0px;">
        <div>
            <label for="">First Text Color</label>
            <input type="color" value={firstTextColor} on:input={(e) => (firstTextColor = e.target.value)} />
        </div>
        <div>
            <label for="">First Text</label>
            <input
            maxlength="120"
            type="text"
            value={firstText}
            on:input={(e) => (firstText = e.target.value)}
            />
        </div>



        <div>
            <label for="">Second Text Color</label>
            <input type="color" value={secondTextColor} on:input={(e) => (secondTextColor = e.target.value)} />
        </div>
        <div>
            <label for="">Second Text</label>
            <textarea
                rows="5" 
                cols="33"
                type="text"
                value={secondText}
                on:input={(e) => (secondText = e.target.value)}
            />
        </div>



        <div>
            <label for="">First Button Background Color</label>
            <input type="color" value={firstButtonColor} on:input={(e) => (firstButtonColor = e.target.value)} />
        </div>
        <div>
            <label for="">First Button Color</label>
            <input type="color" value={firstButtonTextColor} on:input={(e) => (firstButtonTextColor = e.target.value)} />
        </div>
        <div>
            <label for="">First Button Text</label>
            <input
            type="text"
            value={firstButtonText}
            on:input={(e) => (firstButtonText = e.target.value)}
            />
        </div>



        <div>
            <label for="">Second Button Background Color</label>
            <input type="color" value={secondButtonColor} on:input={(e) => (secondButtonColor = e.target.value)} />
        </div>
        <div>
            <label for="">Second Button Color</label>
            <input type="color" value={secondButtonTextColor} on:input={(e) => (secondButtonTextColor = e.target.value)} />
        </div>
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

  </style>
  