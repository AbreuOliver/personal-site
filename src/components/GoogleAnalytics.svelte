<script>
    import { stores } from '@sapper/app';
    const { page } = stores();
    $: {
        if (typeof gtag !== "undefined"){
            gtag("config", "G-NYGB2ZWWCJ", {
            page_path: $page.path
            });
        }
    }
</script>