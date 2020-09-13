<div style="text-align: center;">
    <img src="http://geekgan.top/static/img/pv.png">
</div>

![node-versioin](https://img.shields.io/badge/node-v10+-blue)
![postcss-versioin](https://img.shields.io/badge/postcss-v7.0-blue)
![postcss-px2vw-pv-versioin](https://img.shields.io/badge/postcss--px2vw--pv-v1.1-blue)

# postcss-px2vw-pv

 [Doc ZH-CN 🇨🇳](https://github.com/pomelott/postcss-px2vw-pv/blob/master/zh-cn.md)

PostCSS plugin which transfer px to vw when use pv unit directly.

* if like this, could you please ⭐️star⭐ on github

## Install

```bash
    npm i postcss-px2vm-pv -D
```

```bash
    yarn add postcss-px2vw-pv --dev
```

## Options

| option | type | default | description |
|:---:|:---:|:---:|:---:|
| width | number | 750 | the px-width of design draft |
| decimal | number | 4 | number of reserved decimal places |
| comment | boolean | true | whether to create the comment |

## Fast use

* first to add the plugin to postcss.

```js
    module.exports = {
        plugins: [
            require('postcss-px2vw-pv')
        ]
    }
```

* then set the options of your design draft or use default.
* when the width/height of a div is '500px', then use '500pv' to replace it.

## Samples

* with a design draft of 750

```css
    @keyframes ani {
        from {
            transform: translateY(-20pv);
        }
        to {
            transform: translateY(20pv);
        }
    }
    .box {
        width: 500pv;
        height: 500pv;
        transform: translateX(10pv);
    }
```

* the sample above transferred to:

```css
    @keyframes ani {
        from {
            transform: translateY(-2.6667vw);
        }
        to {
            transform: translateY(2.6667vw);
        }
    }
    .box {
        width: 66.6667vw;
        height: 66.6667vw;
        transform: translateX(1.3333vw);
    }
```
