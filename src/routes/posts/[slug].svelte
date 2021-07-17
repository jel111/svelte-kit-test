<script context="module">

export async function load({page}) {
    try {
            const Post = await import(`../../posts/${page.params.slug}.md`);
            return {
            //Data passed into Svelte component
                props: {
                    Post: Post.default          
                }
            };
    } catch (e) {
        //Redirect
// return {
//     status: 303,
//     redirect: '/posts'
// };
// For staus to work we need to correct outputs
return {
    status: 404,
    error: 'Post not found'
};
    }
}

</script>

<script>
    // import Hello from '../../posts/hello.md';
    export let Post;
</script>

<Post />


