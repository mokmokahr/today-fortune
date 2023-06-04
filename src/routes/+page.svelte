<script>
    import { goto } from "$app/navigation";
    let flipped1 = 0,flipped2 = 0,flipped3 = 0;
</script>
<div id="page">
    <div>
        <h1>오늘의 운세</h1>
    </div>
    <div id="carpet">
            <div class="card" id="card1">
                {#if flipped1 == 0}
                <img src="https://i.pinimg.com/550x/27/51/58/275158db57cd8482c3fc6d3a3d0cd353.jpg" alt="" on:click={()=>{flipped1++}}>
                {:else if flipped1== 1}
                <img src="https://www.db.yugioh-card.com/yugiohdb/get_image.action?type=1&osplang=1&cid=7125&ciid=1&enc=AYEOx4NClwLY1x25vWVFPQ&app=tournament&request_locale=ko" alt="A" on:click={()=>{goto('/result')}}>
                <p>카드를 클릭해보세요!</p>
                {/if}
            </div>

            <div class="card" id="card2">
                {#if flipped2 == 0}
                <img src="https://i.pinimg.com/550x/27/51/58/275158db57cd8482c3fc6d3a3d0cd353.jpg" alt="" on:click={()=>{flipped2++}}>
                {:else}
                <img src="https://www.db.yugioh-card.com/yugiohdb/get_image.action?type=1&osplang=1&cid=7125&ciid=1&enc=AYEOx4NClwLY1x25vWVFPQ&app=tournament&request_locale=ko" alt="A" on:click={()=>{goto('/result')}}>
                <p>카드를 클릭해보세요!</p>
                {/if}
            </div>
            <div class="card" id="card3">
                {#if flipped3 == 0}
                <img src="https://i.pinimg.com/550x/27/51/58/275158db57cd8482c3fc6d3a3d0cd353.jpg" alt="" on:click={()=>{flipped3++}}>
                {:else}
                <img src="https://www.db.yugioh-card.com/yugiohdb/get_image.action?type=1&osplang=1&cid=7125&ciid=1&enc=AYEOx4NClwLY1x25vWVFPQ&app=tournament&request_locale=ko" alt="A" on:click={()=>{goto('/result')}}>
                <p>카드를 클릭해보세요!</p>
                {/if}
            </div>
    </div>
    <div id="footer">
        <p id="crevice">@crevice</p>
        <p id="person">개발:WP목정빈 디자인:WP전주언</p>
    </div>
</div>
<style>
    @import '../style/global.css';
    @font-face {
    font-family: 'Cafe24ClassicType-Regular';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2210-2@1.0/Cafe24ClassicType-Regular.woff2') format('woff2');
    font-weight: normal;
    font-style: normal;
}
    *{
        margin: 0;
        border-radius: 1rem;
        color: white;
    }
    h1{
        margin-top: 1.2rem;
        font-family: 'Cafe24ClassicType-Regular';
    }
    div#page{
        background-image: url('https://img.freepik.com/premium-photo/high-definition-star-field-colorful-night-sky-space-nebula-and-galaxies-in-space-astronomy-concept-background_232070-8070.jpg');
        border-radius: 0;
        display: flex;
        width: 100vw;
        height: 100vh;
        background-color: rgb(132, 0, 247);
        flex-direction: column;
        align-items: center;
    }
    div>img{
        width: 20vw;
        margin: 0.5rem;
    }
    div#carpet{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        background-color: rgb(0, 0, 0);
        width: 80vw;
        height: 83vh;
        margin-top: 1.5rem;
        text-align: center;
        font-family: 'Cafe24ClassicType-Regular';
    }
    div.card:hover{
        transition-delay:100ms;
        transform: scale(105%);
    }
    img:hover{
        border: solid 0.1rem rgb(251, 255, 0);
    }
    div#footer{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    p#crevice{
        font-family: 'Cafe24ClassicType-Regular';
    }
    p#person{
        font-size: 0.7rem;
    }
</style>