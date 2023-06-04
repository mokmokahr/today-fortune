<script>
    import { goto } from "$app/navigation";
    const retest = ()=>{
        goto('/');
    }
</script>

<div>
    <img src="https://www.db.yugioh-card.com/yugiohdb/get_image.action?type=1&osplang=1&cid=7125&ciid=1&enc=AYEOx4NClwLY1x25vWVFPQ&app=tournament&request_locale=ko" alt="">
    <button on:click={()=>{retest()}}>다시하기</button>
</div>
<style>
    @font-face {
        font-family: 'Cafe24ClassicType-Regular';
        src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2210-2@1.0/Cafe24ClassicType-Regular.woff2') format('woff2');
        font-weight: normal;
        font-style: normal;
    }
    div{
        background-color: black;
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    img{
        height: 80vh;
        border-radius: 1.5rem;
    }
    button{
        margin-top: 2rem;
        width: 30vw;
        background-color:white;
        font-family: 'Cafe24ClassicType-Regular';
    }
</style>