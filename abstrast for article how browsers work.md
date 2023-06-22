---
tag: 📥
---

# Which browsers are we talking about
Chrome, Internet Explorer, Firefox, Safari and Opera. And most browsers that are built on **Chromium**
On mobile, the main browsers are Android Browser, iPhone, Opera Mini and Opera Mobile, UC Browser, the Nokia S40/S60 browsers and Chrome, all of which, except for the Opera browsers, are based on **WebKit**.

# The browser's main functionality
The main function of any browser - get web resource you chosen and interptetated hom for human (code -> web page, binary data to pdf file, etc.)

The resource is usually a html document, but may also be a pdf document, video, img or etc.

Browsers UI have a lot of in common with each other:
- **Address bar for inserting URL**
- **Back and forward buttons**
- **Bookmarking button**
- **"Refresh" and "Stop" buttons** to refreshing of stopping loading content of current document
- **Home button to take you to homepage**

These elements are not listed in any specification. Rather, they are the result of years of practice and imitation of one another.

# The browser high-level structure

The browser main components is:
- **The User Interface (UI)**
	- Address bar, back/forward buttons, refresh/stop, etc.
- **The Rendering engine. **
	- Analyze input document and display it.
		- For example, if it HTML document - parse html and css code and display elements to user
- **The Browser engine**
	- Linking UI and Rendering engine
- **Networking**
	- For HTTP/HTTPS requests, etc.
	- All for communicate with other PC
- **UI backend**
	- used for drawing basic widgets like combo boxes and windows. This backend exposes a generic interface that is not platform specific. Underneath it uses operating system user interface methods.
- **JS interpreter**
	- Used to parse and execute JavaScript code.
- **Data storage**
	- Using for save all kind of data: cookies, images, html documents, etc.
	- Browser also support storage mechanisms such as LocalStorage, IndexedDB, WebSQl and FileSystem
	- ![[Browser components .excalidraw]]