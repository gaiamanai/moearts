<script>
    import Button from "./Button.svelte";
    import Sticker_1 from "$lib/images/Group 1.png"
    import Sticker_2 from "$lib/images/Group 2.png"
</script>

<div class="container">
    <div class="content">
        <img src="{Sticker_1}" alt="stickers">
        <div class="title"><h1>
            VISUAL<br />DESIGNER
        </h1>
        <Button button_label="AVAILABLE FOR FREELANCE"></Button>
        </div>
        
        <img src="{Sticker_2}" alt="stickers">
        
    </div>
</div>

<style>
    .container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 600px;
        width: 100%;
    }
    .title
    {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .content {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        width: 100%;
    }
    h1 {
        line-height: 80%;

        letter-spacing: -4px;
        font-size: 88pt;
        font-weight: bold;
        color: #e7e7e7;
    }

    @media (max-width: 1280px) {
    }

    @media (max-width: 1024px) {
    }

    @media (max-width: 768px) {
    }
    @media (max-width: 640px) {
    }
</style>
