<script>
    import Post from "../components/blog/post.svelte";
    import { blogPosts } from "../data/blogposts";
</script>

{#each blogPosts as post}
    <Post
        title={post.title}
        description={post.description}
        postID={post.postID}
        image={post.image} />
{/each}
