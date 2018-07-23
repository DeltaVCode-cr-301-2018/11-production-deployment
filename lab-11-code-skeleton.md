## Code Skeleton

```js
server.js
    Dependencies: express, cors, pg
    Middleware: app.use(cors())
    API Endpoints:
        app.get('/api/v1/books'
    Client Endpoints:
        app.get('*', (req, res) => res.status(403).send('This route does not exist'));

models/

    book.js
        errorCallback(err)       // inits error page if an error
        Book(rawBookObj)         // constructor
        Book.prototype.toHTML()  // render method
        Book.all = []
        Book.loadAll(rows)       // sorts rows of results
        Book.fetchAll(callback)  // $.get(`${  API_URL  }/api/v1/books`)

views/

    book-view.js
        bookView.initIndexPage()

    error-view.js
        errorView.initErrorPage(err)
        
```