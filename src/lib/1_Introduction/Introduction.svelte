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

    const {src, alt, courseName} = data;

</script>

<h1>Hello everyone!</h1>

<img {src} alt="image: {alt}" />
<h3>Course Name: {@html courseName}</h3>


<style>
    h1{
        color: blue;
    }
</style>
