<script>
  const postFetch = async () => {
    const result = await fetch("/api/post", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
      },
      body: "{}",
    })
      .then((res) => res.text())
      .then((text) => text);

    console.log(result);
  };

  const getFetch = async () => {
    const result = await fetch("/api/get", {
      method: "GET",
      headers: {
        "Content-Type": "application/json",
      },
    })
      .then((res) => res.text())
      .then((text) => text);

    console.log(result);
  };
</script>

<h1>Welcome to SvelteKit</h1>
<p>
  Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a>
  to read the documentation
</p>

<button on:click={getFetch}>Get Call</button>
<button on:click={postFetch}>Post Call</button>
