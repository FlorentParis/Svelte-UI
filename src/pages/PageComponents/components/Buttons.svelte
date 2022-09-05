<div id="compo-container">
    <div id="preview">
        <button>
            Test
        </button>
    </div>
    <div id="code-sources">
        <p>
            &lt;button style="margin: 0 auto;"&gt;
            Test
            &lt;/button&gt;
        </p>
    </div>
</div>
<div id="preferencies">
    <div>
        <label for="">Background Color</label>
        <input type="color" />
    </div>

    <div>
        <label for="">Text Color</label>
        <input type="color" />
    </div>

    <div>
        <label for="">Text</label>
        <input type="text" />
    </div>

    <div>
        <label for="">Size</label>
        <select>
            <option>sm</option>
            <option>md</option>
            <option>lg</option>
            <option>xl</option>
        </select>
    </div>

    <div>
        <label for="">Border Radius</label>
        <select>
            <option>1</option>
            <option>1</option>
            <option>1</option>
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
    }
</style>