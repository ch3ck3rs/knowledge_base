# CURL

to post with an image

The -F tells API that is it a multipart-form

	curl -i -X POST -H "Content-Type:multipart/form-data" -F "image=@C:\Users\coffmlv\Pictures\Dilbert.png" -F "summary='This is an image test on curl'" -u rabbit:1835Republic localhost:8000/jobs-api/

[Slack OverFlow](https://stackoverflow.com/questions/12667797/using-curl-to-upload-post-data-with-files)

[Medium](https://medium.com/@petehouston/upload-files-with-curl-93064dcccc76)

---
[terminal](https://ch3ck3rs.github.io/knowledge_base/terminal)

[Home](https://ch3ck3rs.github.io/knowledge_base)
