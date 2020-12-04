<script>
    export let title;
    export let description;
    export let image;
    export let postID;

    //let formattedDate = date.toDateString();
</script>

<style>
  
    a {
        width: 100%;
        border-bottom: 1px solid var(--accent);
        display: block;
        padding: 15px;
        margin: 0px;
    }
    a img {
        display: none;
    }
     
    h1 {
        padding: 0px;
        margin: 0px;
    }

    p {
        padding: 0px;
        margin: 0px;
    }
</style>
<a href="./blog/post?id={postID}">
    <img src={image} alt="" />
    <h1>{title}</h1>
    <p>{description}</p>
</a>
