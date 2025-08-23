---
{"publish":true,"title":"She who weeps","cssclasses":""}
---

<%* 
let title = tp.file.title 
let name = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: What is it?");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  })
}, 200)

-%>