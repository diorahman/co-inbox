
co-inbox
================
Better inbox api based on [visionmedia/co](https://github.com/visionmedia/co) and [andris9/inbox](https://github.com/andris9/inbox)

### Installation
```sh
$ npm install co-inbox
```

### Usage
```js
var inbox = Object.create(Inboxes);
var client = yield inbox.createConnection(false, 'imap.gmail.com', {
  secureConnection: true,
  auth: {
    user: 'yorkiefixer@gmail.com',
    pass: 'xxxxxxxxx'
  },
  debug: true
});

var mailboxes = yield inbox.listMailboxes();
console.log(mailboxes);

inbox.close();
```
NB: for more infomation on API, you could visit [andris9/inbox](https://github.com/andris9/inbox)

### Supported API

* createConnection(port, host, option)

* listMailboxes()

* getMailbox(path)

* openMailbox(path)

* listMessages(from, limit)

* listMessagesByUID(first, last)

* listFlags(from, limit)

* search(query, isUID)

* fetchFlags(uid)

* addFlags(uid, flags)

* removeFlags(uid, flags)

* storeMessage(message, flags)

* copyMessage(uid, destination)

* moveMessage(uid, destination)

* deleteMessage(uid)

### License
MIT