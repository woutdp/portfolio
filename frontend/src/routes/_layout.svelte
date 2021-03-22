<script>
    import Footer from '../components/Footer.svelte'

    export let segment
</script>

<style global lang="stylus">
    @import '../styles/global'
    @import '../styles/highlight'

    .grid-container
        min-height 100%
        display grid
        grid-template-rows 1fr auto
        grid-template-areas:
            'main' \
            'footer'

    main
        grid-area main
</style>

<div class="grid-container">
    <main>
        <slot segment="{segment}"/>
    </main>

    <Footer/>
</div>
