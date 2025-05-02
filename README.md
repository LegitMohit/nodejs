
# TASK 10 :- 👇 
```
public_users.get('/async', async function (req, res) {  try {    const bookList = await getBookListAsync('http://localhost:5000/'); //    res.json(bookList);  } catch (error) {    console.error(error);    res.status(500).json({ message: "Error retrieving book list" });  }}); 
```

# TASK 11 :- 👇 
```
public_users.get('/async/isbn/:isbn', async function (req, res) {  try {    const requestedIsbn = req.params.isbn;    const book = await getBookListAsync("http://localhost:5000/isbn/" + requestedIsbn);    res.json(book);  } catch (error) {    console.error(error);    res.status(500).json({ message: "Error retrieving book details" });  }});
```

# TASK 12 :- 👇
```
public_users.get('/async/author/:author', async function (req, res) {  try {    const requestedAuthor = req.params.author;    const book = await getBookListAsync("http://localhost:5000/author/" + requestedAuthor);    res.json(book);  } catch (error) {    console.error(error);    res.status(500).json({ message: "Error retrieving book details" });  }});
```

# TASK 13 :- 👇
```
public_users.get('/async/title/:title', async function (req, res) {  try {    const requestedTitle = req.params.title;    const book = await getBookListAsync("http://localhost:5000/title/" + requestedTitle);    res.json(book);  } catch (error) {    console.error(error);    res.status(500).json({ message: "Error retrieving book details" });  }});
```
