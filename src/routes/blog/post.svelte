<script>
    import { stores } from "@sapper/app";
    import { blogPosts } from "../../data/blogposts";

    const { page } = stores();
    $: id = $page.query.id;
    $: post = blogPosts.find((post) => post.postID == id);

    // const postID = page.path.split("?")[0];
    // const post = blogPosts.find((post) => post.postID == postID);
</script>

<style>
    h1 {
        padding: 0px;
        margin: 0px;
    }
    post {
        padding: 15px;
        display: block;
    }
</style>

<post>
    <h1>{post.title}</h1>
    <p>
        {@html post.post}
    </p>
    <div class="a2a_kit a2a_kit_size_32 a2a_default_style">
        <!-- svelte-ignore a11y-missing-content -->
        <a class="a2a_dd" href="https://www.addtoany.com/share" />
        <!-- svelte-ignore a11y-missing-content -->
        <!-- svelte-ignore a11y-missing-attribute -->
        <a class="a2a_button_facebook" />
        <!-- svelte-ignore a11y-missing-content -->
        <!-- svelte-ignore a11y-missing-attribute -->
        <a class="a2a_button_twitter" />
        <!-- svelte-ignore a11y-missing-content -->
        <!-- svelte-ignore a11y-missing-attribute -->
        <a class="a2a_button_email" />
        <!-- svelte-ignore a11y-missing-content -->
        <!-- svelte-ignore a11y-missing-attribute -->
        <a class="a2a_button_facebook_messenger" />
        <!-- svelte-ignore a11y-missing-content -->
        <!-- svelte-ignore a11y-missing-attribute -->
        <a class="a2a_button_linkedin" />
        <!-- svelte-ignore a11y-missing-content -->
        <!-- svelte-ignore a11y-missing-attribute -->
        <a class="a2a_button_copy_link" />
    </div>
    <script async src="https://static.addtoany.com/menu/page.js">
    </script>
</post>
