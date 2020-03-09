# markdown-sample

## 必要なパッケージのインストール

```js
npm install --save-dev html-loader markdown-loader
```

## vue.config.js

```js
module.exports = {
  configureWebpack: {
    module: {
      rules: [
        {
          test: /\.md$/,
          use: [
            {
              loader: "html-loader"
            },
            {
              loader: "markdown-loader",
              options: {
                /* your options here */
              }
            }
          ]
        }
      ]
    }
  }
};

```

## 〇〇.js

`@/assets/markdowns/sample.md` にマークダウンが配置されているとして...

```vue
<template>
  <div>
    <div v-html="sampleMd"></div>
  </div>
</template>

<script>
import sampleMd from "@/assets/markdowns/sample.md";

export default {
  created() {
    this.sampleMd = sampleMd;
  }
};
</script>

```
