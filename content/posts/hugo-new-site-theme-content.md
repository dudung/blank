+++
title = 'hugo new site theme content'
date = 2024-01-10T20:38:58+07:00
draft = false
tags = ['hugo']
+++
Use cmd and git bash on Windows 11.


## clone github repo
```
$ git clone https://github.com/dudung/blank
Cloning into 'blank'...
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 7 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (7/7), done.
```


## force to create hugo new site
```
D:\>hugo new site blank -f
Congratulations! Your new Hugo site was created in D:\blank.

Just a few more steps...

1. Change the current directory to D:\blank.
2. Create or install a theme:
   - Create a new theme with the command "hugo new theme <THEMENAME>"
   - Install a theme from https://themes.gohugo.io/
3. Edit hugo.toml, setting the "theme" property to the theme name.
4. Create new content with the command "hugo new content <SECTIONNAME>\<FILENAME>.<FORMAT>".
5. Start the embedded web server with the command "hugo server --buildDrafts".

See documentation at https://gohugo.io/.
```


## create default theme
```
D:\>cd blank

D:\blank>hugo new theme default
Creating new theme in D:\blank\themes\default
```


## modify hugo.toml
```
D:\blank>notepad hugo.toml
```

```
baseURL = 'https://dudung.github.io/blank'
languageCode = 'en-us'
title = 'blank'
theme = 'default'
```


## delete generated posts
```
D:\blank>del themes\default\content\_index.md

D:\blank>del themes\default\content\posts\*.*
D:\blank\themes\default\content\posts\*.*, Are you sure (Y/N)? y

D:\blank>del themes\default\content\posts\post-3\*
D:\blank\themes\default\content\posts\post-3\*, Are you sure (Y/N)? y

D:\blank>rmdir themes\default\content\posts\post-3

D:\blank>rmdir themes\default\content\posts

D:\blank>rmdir themes\default\content
```


## create new post
```
D:\blank>hugo new content posts\hugo-new-site-theme-content.md
Content "D:\\blank\\content\\posts\\hugo-new-site-theme-content.md" created
```

```
D:\blank>notepad content\posts\hugo-new-site-theme-content.md
```


## run hugo server
```
D:\blank>hugo server
Watching for changes in D:\blank\{archetypes,assets,content,data,i18n,layouts,static,themes}
Watching for config changes in D:\blank\hugo.toml, D:\blank\themes\default\hugo.toml
Start building sites …
hugo v0.118.2-da7983ac4b94d97d776d7c2405040de97e95c03d+extended windows/amd64 BuildDate=2023-08-31T11:23:51Z VendorInfo=gohugoio


                   | EN
-------------------+-----
  Pages            |  9
  Paginator pages  |  0
  Non-page files   |  0
  Static files     |  1
  Processed images |  0
  Aliases          |  0
  Sitemaps         |  1
  Cleaned          |  0

Built in 10 ms
Environment: "development"
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/blank/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```
