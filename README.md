# PhotoViewer

该图片查看器是模仿微信朋友圈查看图片有感而编写

**使用：**

```Kotlin
PhotoViewer
          .setData(图片链接List<String>)
          .setCurrentPage(现在是哪页)
          .setPicSize(当前图片的宽, 当前图片的高)
          .setPicSpace(图片之间的横距离, 图片之间的竖距离（如果只有一行则写0）)
          .setCountOfRow(一行几个图片)
          .setClickViewLocation(点击的位置 array[2] [0]为x [1]为y)
          .setShowImageViewInterface(object : PhotoViewer.ShowImageViewInterface {
              override fun show(iv: ImageView, url: String) {
               
                // 设置自己加载图片的框架来加载图片
                  Glide.with(iv.context).load(url).into(iv)
              }
          })
          .start(this)
```


**获取上述代码中的location**

```Kotlin
int[] location = new int[2];
// 这样就为location赋值了
holder.itemView.getLocationInWindow(location);
```

---





