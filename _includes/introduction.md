<div id="category"></div>

### Back ground

My friend (Cloud) touch jekyll and recommend that to me. I like the simple way like this to write blogs, so I decide to make one to document down the tech stuff and my life.  Thanks to my wife be with me at the coffee shop to create this.

Hello World, here we are.

### Some reference

[jekyll](#)
[jekyll bootstrap](http://jekyllbootstrap.com/)
[http://www.mceiba.com/](http://www.mceiba.com/develop/jekyll-introduction.html)

### Special high light

#### code highlight support

After reading several documents, finally find out a way to support code block highlight which I think would be very useful.

{% highlight c %}
/* hello world demo */
#include <stdio.h>
int main(int argc, char **argv)
{
    printf("Hello, World!\n");
    return 0;
}
{% endhighlight %}

#### page content index generation

I think it would be easy to let people to locate the content they interest in by clicking the index. Thanks for helps from [here](https://gist.github.com/allwefantasy/6238442), an index of the page can be generated automatically.

What we need to do is to add below tag into the md file head.

{% highlight html %}
<div id="category"></div>
{% endhighlight %}


#### use duoshuo comments plug-in

For this Blog's audience likely may from China, so a Chinese comments plugin which name [duoshuo](www.duoshuo.com) was chosen. So for now you can login with QQ/weibo/RenRen/Douban to make your comments.

#### picture repository

To be simple, we can use the git repository as the picture repository, but considering the space is limited, so need to registry a repository from external.


