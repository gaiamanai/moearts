<script>
    import { ChevronRight } from "@lucide/svelte";
    export let button_label = "Default label";
</script>

<a href="#" class="button">
    <div class="content">
        <p>{button_label}</p>
        <ChevronRight width="24px" height="24px" color="#f7f7f7" />
    </div>
</a>

<style>
    .button {
        text-decoration: none;
        display: inline-flex;
        height: 48px;
        padding: 8px 24px;
        justify-content: center;
        align-items: center;
        gap: 16px;
        border-radius: 32px;
        background: #1b1b1b;
        border: 1px, solid, #f7f7f7;
        box-shadow: 0px 4px 8px 0px rgba(0, 0, 0, 0.15);
        z-index: 5;
        transition: 0.3s;
    }
    .button:hover{
        background: #596bee;
        transition: 0.3s;
        border: none;
    }
    .content {
        display: flex;
        align-items: center;
        gap: 8px;
    }
    p {
        color: #efefef;
        text-align: center;
        font-size: 18px;
        font-style: normal;
        font-weight: 600;
        line-height: 16px; /* 88.889% */
        letter-spacing: -0.18px;
    }
    @media (max-width: 1010px) {
        p{ 
            font-size: 16px;
    }
    
    
}
@media (max-width: 650px) {
        p{ 
            font-size: 14px;
    }
    .button {
       
        padding: 6px 18px;
    }
    
}
@media (max-width: 375px) {
    p{ 
            font-size: 12px;
    }
    .button {
       
       padding: 2px 16px;
   }
  }
</style>
