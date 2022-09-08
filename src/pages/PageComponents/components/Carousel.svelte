<script>
    let textValue = ""

    const EventClickerStats = (event) => {
        let carousel = document.querySelector('#container-items');
        let width = carousel.clientWidth;

        if(event.target.id == 'left') {
            if(carousel.scrollLeft == 0) {
                carousel.scrollLeft += width*2
            } else {
                carousel.scrollLeft -= width;
            }
            } else if (event.target.id == 'right') {
            if(carousel.scrollLeft != width*2 && carousel.scrollLeft <= width*2 - 1) {
                carousel.scrollLeft += width;
            } else {
                carousel.scrollLeft = 0
            }
        }
    }
</script>

<div id="compo-container">
    <div id="preview">
        <div id="carousel">
            <div id="container">
                <img src="https://cdn-icons-png.flaticon.com/512/6423/6423874.png" id="left" alt="arrow" on:click={(e) => EventClickerStats(e)} />
                <div id="container-items">
                    <div>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Maiores suscipit aut at nesciunt impedit ad explicabo laudantium assumenda! Magni a placeat perferendis, architecto cupiditate molestias tempore perspiciatis in laudantium voluptatibus!</div>
                    <div>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates sed ducimus eum consectetur eos ipsum suscipit ab molestias nobis aut ea eius aperiam est, laborum possimus optio veniam minus quae!</div>
                    <div>Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime sunt debitis odit at voluptate expedita quam deleniti enim ratione magni illo voluptatem dolore quas corrupti quibusdam corporis, itaque voluptates! Facere!</div>
                </div>
                <img src="https://www.innodura.fr/wp-content/uploads/1992/01/right-arrow.png" id="right" alt="arrow" on:click={(e) => EventClickerStats(e)} />
            </div>
        </div>
    </div>
    <div id="code-sources">
        <h2>Code Sources :</h2>
        <p>
            &lt;script&gt; <br />
            &#160;const EventClickerStats = (event) =&gt; &#123; <br/>
            &#160;&#160;let carousel = document.querySelector('#container-items'); <br/>
                    &#160;&#160;let width = carousel.clientWidth; <br/>
            
                    &#160;&#160;&#160;if(event.target.id == 'left') &#123;<br/>
                    &#160;&#160;&#160;&#160;if(carousel.scrollLeft == 0) &#123; <br />
                    &#160;&#160;&#160;&#160;&#160;carousel.scrollLeft += width*2 <br />
                    &#160;&#160;&#160;&#160;&#125;else &#123; <br />
                    &#160;&#160;&#160;&#160;&#160; carousel.scrollLeft -= width; <br />
                    &#160;&#160;&#160;&#160;&#125; <br />
                    &#160;&#160;&#160;&#125; else if (event.target.id == 'right') &#123; <br />
                    &#160;&#160;&#160;&#160;if(carousel.scrollLeft != width*2 && carousel.scrollLeft &lt;= width*2 - 1) &#123; <br />
                    &#160;&#160;&#160;&#160;&#160;carousel.scrollLeft += width; <br />
                    &#160;&#160;&#160;&#160;&#125; else &#123; <br />
                    &#160;&#160;&#160;&#160;&#160;carousel.scrollLeft = 0 <br />
                    &#160;&#160;&#160;&#160;&#125; <br />
                    &#160;&#160;&#160;&#125; <br/>
                    &#160;&#125; <br/>
            &lt;/script&gt;
            <br /><br />

            &lt;div id="carousel"&gt; <br />
            &#160; &lt;div id="container"&gt; <br />
            &#160; &#160; &lt;img src="https://cdn-icons-png.flaticon.com/512/6423/6423874.png" id="left" alt="arrow" on:click=&#123;(e) =&gt; EventClickerStats(e)&#125; /&gt; <br />
            &#160; &#160;&lt;div id="carousel"&gt; <br />
                        &#160; &#160; &#160;&lt;div&gt; <br />
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam sunt eveniet illo dolore fugit quis impedit dolorem possimus consequuntur ut, veritatis ab consequatur minus alias praesentium ratione iure velit quisquam.
                        &#160; &#160; &#160;&lt;/div&gt; <br />
                        &#160; &#160; &#160;&lt;div&gt; <br />
                            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Impedit nesciunt dignissimos quis accusantium laboriosam at temporibus ducimus officiis voluptatibus nam, molestiae error omnis ab. Suscipit sed iure quibusdam corporis asperiores.
                        &#160; &#160; &#160;&lt;/div&gt; <br />
                        &#160; &#160; &#160;&lt;div&gt; <br />
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis ipsum excepturi eveniet minima. Quidem, quae magnam? Omnis ullam sapiente officiis, neque dolores quos enim culpa, natus commodi fuga libero vero?
                        &#160; &#160; &#160;&lt;/div&gt; <br />
                        &#160; &#160;&lt;/div&gt; <br />
                        &#160; &#160;&lt;img src="https://www.innodura.fr/wp-content/uploads/1992/01/right-arrow.png" id="right" alt="arrow" on:click=&#123;(e) =&gt; EventClickerStats(e)&#125; style="" /&gt; <br />
                        &#160; &lt;/div&gt; <br />
            &lt;/div&gt;

            <br /><br />

            &lt;style&gt; <br /> 
            #carousel &#123; <br />
                &#160; display: flex; <br />
                &#160; align-items: center; <br />
                &#160; justify-content: center; <br />
                &#160; position: relative; <br />
                &#160; width: 100%; <br />
            &#125; <br /> <br />
            #container &#123; <br />
                &#160; max-width: 1440px; <br />
                &#160; padding: 20px 0; <br />
                &#160; width: 100%; <br />
                &#160; height: 100%; <br />
                &#160; display: flex; <br />
                &#160; align-items: center; <br />
            &#125; <br /> <br />
            #container > img &#123; <br />
                &#160; height: 140px; <br/>
                &#160; cursor: pointer; <br/>
            &#125; <br /> <br />
            #container-items &#123; <br />
                &#160; overflow-x: scroll; <br />
                &#160; scroll-snap-type: x mandatory; <br />
                &#160; box-sizing: border-box; <br />
                &#160; scroll-behavior: smooth; <br />
                &#160; display: flex; <br />
            &#125; <br /> <br />
            #container-items::-webkit-scrollbar  &#123; <br />
                &#160; display: none; <br/>
            &#125; <br /> <br />
            #container-items > div &#123; <br />
                &#160; min-width: 100%; <br/>
                &#160; display: flex; <br/>
                &#160; align-items: center; <br/>
                &#160; justify-content: center; <br/>
            &#125; <br /> <br />
            &lt;/style&gt;
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
        max-height: 500px;
        overflow-y: scroll;
    }

    #preferencies {
        display: flex;
        gap: 30px;
        padding: 20px 90px;
        justify-content: center;
    }

    #carousel {
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        width: 100%;
    }

    #container {
        max-width: 1440px;
        padding: 20px 0;
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
    }

    #container > img {
        height: 140px;
        cursor: pointer;
    }

    #container-items {
        overflow-x: scroll;
        scroll-snap-type: x mandatory;
        box-sizing: border-box;
        scroll-behavior: smooth;
        display: flex;
    }

    #container-items::-webkit-scrollbar {
        display: none;
    }

    #container-items > div {
        min-width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>