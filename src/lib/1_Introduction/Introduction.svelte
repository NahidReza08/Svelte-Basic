<!-- 
    Only one script tag and one style tag is accepted per component
    Both script and style tag accept an attribute lang
    For using typscript, pass lang="ts" in script tag. (default js)
    For using saas, pass lang="saas" in style tag. (default css) 
-->

<script>
    const data = {
        src: '../dynamic-learning-logo.svg',
        alt: 'Dynamic Learning Logo',
        courseName: '<u>Svelte(Basic)</u>'
    }
</script>

<h1>Hello everyone!</h1>

<img src={data?.src} alt="image: {data?.alt}" />
<h3>Course Name: {@html data?.courseName}</h3>

<style>
    h1{
        color: blue;
    }
</style>
