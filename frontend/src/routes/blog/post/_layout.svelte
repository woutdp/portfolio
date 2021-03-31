<script context='module'>
    export async function preload({path}) {
        return this.fetch(`${path}.json`).then(r => r.json()).then(post => {
            return {
                post,
                path
            }
        })
    }
</script>

<script>
    import Navigation from '../../../components/Navigation.svelte'

    export let post
    export let path

    let url = `https://wout.space${path}`
</script>

<svelte:head>
    <title>{post.title}</title>
    <link rel="canonical" href="{url}" />
    <meta name="Description" content={post.excerpt} />

    <meta property="og:url" content="{url}" />
    <meta property="og:type" content="article" />
    <meta property="og:title" content={post.title} />
    <meta property="og:description" content={post.excerpt} />

    <meta name="twitter:card" content="summary" />
    <meta name="twitter:title" value={post.title} />
    <meta name="twitter:description" content={post.excerpt} />
    <meta name="twitter:label1" value="Published on" />
    <meta
            name="twitter:data1"
            value={new Date(post.printDate).toLocaleDateString(undefined, {
            year: 'numeric',
            month: 'short',
            day: 'numeric'
        })} />
    <meta name="twitter:label2" value="Reading Time" />
    <meta name="twitter:data2" value={post.printReadingTime} />
</svelte:head>

<Navigation/>
<section class="section">
    <div class="container blog">
        <div class="post">
            <header>
                <h1>{post.title}</h1>
                <p>{post.printDate} ~ {post.printReadingTime}{#if post.draft} ~ <i>draft</i>{/if}</p>
            </header>
            <article>
                <slot/>
            </article>
            <hr />
        </div>
    </div>
</section>
