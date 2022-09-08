<script>
  let bgc = "#56a1f0";
  let textColor = "#f2eded";
  let borderRadius = "2px";
</script>

<div id="compo-container">
    <div id="preview">
        <div id="modal" style="border-radius: {borderRadius}">
            <h2 id="titre" style="color: {bgc}">Sign in</h2>
            <form action="">
                <div id="input-group">
                    <label for="">Email</label>
                    <input type="email" placeholder="Enter Email"/>
                    <label for="">Password</label>
                    <input type="email" placeholder="Password"/>
                </div>
                <div id="option">
                    <div id="checkbox">
                        <input type="checkbox">
                        <label for="">Remember me</label>
                    </div>
                    <a href="#" style="color: {bgc}">Forgot password?</a>
                </div>
                <button type="submit" style="background-color: {bgc}; color:{textColor}; border-radius:{borderRadius}">Sign in</button>
                <p>Not a member? <a href="#" style="color: {bgc}">Register</a></p>
            </form>
        </div>
    </div>
    <div id="code-sources">
        <h2>Code Sources</h2>
        <p>
            &lt;div id="modal" &gt;<br />&#160;
            &lt;h2 id="titre" &gt; Sign in &lt;/h2&gt; <br />&#160;
            &lt;form action=""&gt;<br />&#160; &#160;

            &lt;div id="input-group" &gt; <br />&#160; &#160; &#160;
            &lt;label name="" &gt; Email &lt;/label&gt;<br />&#160; &#160; &#160;
            &lt;input type="email" placeholder="Enter Email" /&gt;<br />&#160; &#160; &#160;
            &lt;label name="" &gt; Password &lt;/label&gt;<br />&#160; &#160; &#160;
            &lt;input type="password" placeholder="Enter password" /&gt;<br />&#160; &#160;
            &lt;/div&gt<br/>&#160; &#160;

            &lt;div id="option"&gt;<br/>&#160; &#160; &#160;
            &lt;div id="checkbox"&gt;<br/>&#160; &#160; &#160; &#160;
            &lt;input type="checkbox" &gt;<br/>&#160; &#160; &#160; &#160;
            &lt;label &gt; Remember me &lt;/label&gt;<br/>&#160; &#160; &#160;
            &lt;/div&gt;<br/>&#160; &#160; &#160;
            &lt;a href="#" &gt; Forgot password? &lt;/a&gt; <br/>&#160; &#160;
            &lt;/div&gt;<br/> &#160;&#160;

            &lt;button type="submit" &gt;Sign in&lt;/button&gt;<br>&#160; &#160;
            &lt;p&gt;Not a member?&lt;a href="#" &gt;  Register&lt;/a&gt;&lt;/p&gt;<br>&#160;
            &lt;/form&gt;<br />
            &lt;/div&gt; <br> <br>

            &lt;style&gt; <br />
            #modal &#123; <br />&#160;
            border-radius: {borderRadius}; <br />&#160; width: 300px; <br />&#160;
            border: 1px solid; <br />&#160; padding: 30px; <br />
            &#125; <br>
            #titre &#123; <br />&#160;
            color: {bgc}; <br />&#160; <br />
            &#125;<br>
            #input-group &#123; <br />&#160;
            display: flex; <br />&#160; flex-direction: column; <br />&#160; margin-bottom : 5px; <br />&#160;<br />
            &#125;<br>
            label, input &#123; <br />&#160;
            margin-bottom : 10px ; <br />&#160; height : 20px ; <br />&#160;<br />
            &#125;<br>
            #option &#123; <br />&#160;
            display : flex ; <br />&#160; justify-content : space-between ; <br />&#160; align-items : center ; <br /> &#160; margin-bottom: 10px ;<br />
            &#125;<br>
            button &#123; <br />&#160;
            width : 300px ; <br/>&#160; height : 30px; <br/>&#160; border : none;<br/>&#160; color : {textColor};<br/>&#160; background-color : {bgc};<br/>
            &#125;<br>
            a &#123; <br />&#160;
            color : {bgc} ;<br />
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
    #preview {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    #compo-container {
        padding: 20px 90px;
        display: grid;
        grid-template-columns: 1fr 1fr;
    }

    #preview {
        display: flex;
        flex-direction: column;
        align-items: center;
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

    #modal{
        width: 300px;
        border: 1px solid;
        padding: 30px;
    }

    #input-group{
        display: flex;
        flex-direction: column;
        margin-bottom: 5px;
    }

    label, input{
        margin-bottom: 10px;
        height: 20px;
    }

    #option{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 10px;
    }

    button{
        width: 300px;
        height: 30px;
        border:none;
    }

</style>