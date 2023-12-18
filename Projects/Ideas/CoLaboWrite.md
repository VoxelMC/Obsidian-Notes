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