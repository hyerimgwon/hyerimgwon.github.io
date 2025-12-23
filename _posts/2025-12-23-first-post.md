---
title:  "와 메인페이지에 드디어 올라갔다"
mathjax: true
layout: post
categories: media
---

![이미지](/assets/dew.png)


## 해냈다

드디어 사진넣기도했다 너무힘들다 내일 이어서 해야겠당 ㅎㅎ<br>
아래는 이거 만드신 분이 어떻게 코드이미지영상등등을 넣는지 알려주신 것 같으니 지우지 말아야겠음<br>
안녕~ hola~ 

## Code

Embed code by putting `{{ "{% highlight language " }}%}` `{{ "{% endhighlight " }}%}` blocks around it. Adding the parameter `linenos` will show source lines besides the code.

{% highlight c linenos %}

static void asyncEnabled(Dict* args, void* vAdmin, String* txid, struct Allocator* requestAlloc)
{
    struct Admin* admin = Identity_check((struct Admin*) vAdmin);
    int64_t enabled = admin->asyncEnabled;
    Dict d = Dict_CONST(String_CONST("asyncEnabled"), Int_OBJ(enabled), NULL);
    Admin_sendMessage(&d, txid, admin);
}

{% endhighlight %}

## Images

Upload an image to the *assets* folder and embed it with `![title](/assets/name.jpg))`. Keep in mind that the path needs to be adjusted if Jekyll is run inside a subfolder.

![Flower](https://user-images.githubusercontent.com/4943215/55412447-bcdb6c80-5567-11e9-8d12-b1e35fd5e50c.jpg)

[Flower](https://unsplash.com/photos/iGrsa9rL11o) by Tj Holowaychuk

## Embedded content

You can also embed a lot of stuff, for example from YouTube, using the `embed.html` include.

{% include embed.html url="https://www.youtube.com/embed/oa-Yp1QnyAc?si=g7pIn8bSxo4x4n8k" %}