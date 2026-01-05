<script>
  let { data } = $props();
</script>

<p>book {data.bookId}</p>

<p>Current book id: {data.bookId}</p>
<p>Next book id: {parseInt(data.bookId) + 1}</p>

<p><a href="/books/{parseInt(data.bookId) + 1}">Next book</a></p>


<!-- Another way to prevent the components from updating with new properties when navigating dynamics routes


<script>
  let { data } = $props();
  let bookId = $derived(() => parseInt(data.bookId)); // using the derived rune to create a var that keeps track of changes to data
  let nextBookId = $derived(() => bookId + 1);
</script>


<p>book {data.bookId}</p>

<p>Current book id: {bookId}</p>
<p>Next book id: {nextBookId}</p>

<p><a href="/books/{nextBookId}">Next book</a></p> -->

<!-- the following does not use derived runes and will stop the component from updating on navigation
<script>
  let { data } = $props();
  let nextBookId = parseInt(data.bookId) + 1;
</script>

<p>book {data.bookId}</p>

<a href="/books/{nextBookId}">Next book</a> -->
