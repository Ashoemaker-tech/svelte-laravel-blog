<script context='module'>

    const headers = {
        'Accept': 'application/json',
        'Content-Type': 'application/json'
    }
    export async function load({fetch}) {
        const res = await fetch('http://localhost:8000/api/posts', { headers })
        const data = await res.json()
        console.log(data);
        if(res.ok){
            return{
                props: { posts: data.results }
            }
        }
    }
</script>

<!-- <PostSection /> -->






 



