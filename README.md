# Gitbook Simple Page TOC Plugin

*  "<!-- toc -->" is NOT **compatible** with some local markdown editor, like Typora and MWeb.
* So i change it to **[TOC]**, which i can still keep it in local, don't need to change.

## Usage

### Installation

Add the plugin to your `book.json`:

```
{
	"plugins" : [ "simple-page-toc@git+https://github.com/erictt/gitbook-plugin-simple-page-toc.git" ]
}		
```



### Create TOC

Place a `[TOC]` code comment somewhere into your text. Generating your GitBook inserts a table of contents immediately after this comment.

### Optional configuration

You can add the following configuration params to your `book.json`:

```
{
	"plugins" : [ 
		"simple-page-toc@git+https://github.com/erictt/gitbook-plugin-simple-page-toc.git" 
	],
	"pluginsConfig": {
		"simple-page-toc": {
			"maxDepth": 3,
			"skipFirstH1": true
   		}
	}
}			
```

Name        | Type    | Default | Description 
----------- | ------- | ------- | ------------
maxDepth    | Number  |       3 | Use headings whose depth is at most maxdepth.
skipFirstH1 | Boolean |    true | Exclude the first h1-level heading in a file.

## Changelog

* 0.1.1 Releases:
  * 0.1.1 use [TOC] as the mark of "table of contents"
  * 0.1.0 First release
  * 0.1.1 Fixed invalid config example in README (thanks at15) 
