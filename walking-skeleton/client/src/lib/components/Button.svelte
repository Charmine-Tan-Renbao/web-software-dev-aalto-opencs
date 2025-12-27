<script>
  let text = $state("");

  const textChanged = (event) => {
    text = event.target.value;
  };
</script>

<p>Text: {text}</p>
<input type="text" oninput={textChanged} />