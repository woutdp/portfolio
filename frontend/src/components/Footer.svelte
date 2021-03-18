<script>
    let currentYear = new Date().getFullYear()
</script>

<style lang="stylus">
    @import '../styles/variables'

    footer
        grid-area: footer;
        background-color: background
        display: flex;
        flex-direction: column;
        padding: 40px 20px;

        +mobile()
            flex-direction: column

    ul
        display: flex
        align-items: center
        justify-content: center
        text-align: center
        min-width: 100%
        margin: 0
        padding: 0
        margin-bottom: 20px

        :not(:first-child)
            margin-left: 20px

    li
        display: block

    p
        margin: 0
        text-align: center
</style>

<footer>
    <ul>
        <li><a rel="noopener" target="_blank" href="https://github.com/woutdp">GitHub</a></li>
        <li><a rel="noopener" target="_blank" href="https://www.linkedin.com/in/woutdp/">LinkedIn</a></li>
        <li><a rel="noopener" target="_blank" href="mailto:contact@wout.space">Email</a></li>
    </ul>
    <p>
        © { currentYear } Made by Wout De Puysseleir
        with&nbsp;&lt;3,&nbsp;<a rel="noopener" target="_blank" href="https://svelte.dev/">Svelte</a>&nbsp;&&nbsp;<a rel="noopener" target="_blank" href="https://sapper.svelte.dev/">Sapper</a>&nbsp;-&nbsp;<a rel="noopener" target="_blank" href="https://github.com/woutdp/wout.space">Source Code</a>
    </p>
</footer>
