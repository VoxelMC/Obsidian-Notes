Alternate name: ReiterWrite, IterWriter

**Live Markdown Editor**

## Description

CoLaboWrite is a live online collaborative Markdown editor. It will feature a live updating preview pane - rendered on the client - and a git blame-like provenance system. It will also feature a review mode in which comments can be made, and read-only notes.

## Notes

If called `CoLaboWrite`, each "note" will be called a `Lab` or `Laboratory`
If called `IterWriter`, each "note" will be called an `iteration`, and new ones will be created by "calling `next()`" (clicking a button labelled `next();`)

The preview pane and editor pane will be rendered on the client-side. On every edit, the new data is sent to the server in a message (with some debounce time), processed, verified, then sent back out to everyone connected to the socket.

```
Write in Editor --> Message sent to server --> Server renders MD at 
```

It is called Collabowrite!
- Credit to Ana and Sarah

First, let's try markdown rendering on the client side, and content changing with webhooks.
Basically, it will mostly be client-side logic - somehow, I would like to preload things as much as possible, but for now this will work.

ViewTransitions is a must!!

**Incremental Markdown Renderer** is also at foot. I want to benchmark remark vs [this incremental renderer](https://github.com/yhatt/markdown-it-incremental-dom).

If possible, i would like to incrementally render *using* remark, so I will need to make some logic for that.

## Tech
- Astro
- Web-socket

## Roadmap

- Create Landing Page
- Create Dashboard (Probably just going to be the landing page)
- Create Editor
- Create Preview Pane
- Add Accounts
- Add Blame Feature
- Make Editor Collaborative
- Create Preview Reviewer
- Create Web API for Data Handling
	- Reading and Writing Labs
	- Storing Review Comments and Positions
	- Connecting Collaboration Sockets


### Design

Notes are created by a button labeled `experiment.next()`
Groups are called `ColLaboratories` (`ColLaboratory`)
Dark-ish colour theme would be nice. Allow easy contributions for new theme colours.


### Editor

I will try to use Qwik for this, so it resumes *after* the first fetch.
Using CodeMirror works already. - Feb 8 Done Tentative

#### Page Load

#### Editing

##### Incremental Engine
The https://github.com/yhatt/markdown-it-incremental-dom package should work, but it *is* 6 years old. I hope that it can keep up! - Feb 7 Done Tentative



#### Data Transfer

#### Privacy

Should be able to set labs to 

#### Protocol

Each edit event is sent to the server with the following: 
```ts
const message = {
	editor: Person,
	changes: Changes,
	
}
```

### Server

#### Documents

Every document has an id
IDs are used for identifying WebSockets

There needs to be an auth layer for the websocket connection
- Only sends messages if authenticated
- Only receives messages if authenticated or public readonly
- Only connects if the person has an account. Otherwise, only a snapshot can be provided.

When does the websocket record and save to the database? Surely not on every change, so there needs to be a debounce time.


