<script>
    import MarkdownIt from 'markdown-it'

    export let currentRoute = null
    const md = new MarkdownIt()
    let currentMdText = ''
    let doDelay = false

    $: renderedContent = md.render(currentRoute.meta.pageText || '')
</script>

<div class="page-content">
    <article>
        {@html renderedContent}
    </article>
</div>