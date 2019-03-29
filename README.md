# area-puppeteer
* [area-puppeteer](https://github.com/dwqs/area-puppeteer)

## 数据来源
* 国家统计局：[统计用区划代码和城乡划分代码](http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/2016/index.html)
* 国家民政部：[中华人民共和国行政区划代码](http://www.mca.gov.cn/article/sj/tjbz/a/)

## 数据更新

```
git clone git@github.com:dwqs/area-puppeteer.git
npm i
npm start // 生成市县区数据
npm run format // 格式化数据
```

生成的数据包含两份：`cities.js` 和 `areas.js`，前者是市级数据，后者是县区数据

格式化后会生成两份数据：`pca.js` 和 `pcaa.js`，前者仅省市数据，后者包含省市区数据

```js
import Data from 'path/to/pcaa';

Data['86']
// 所有省份：{'110000': '北京市', '120000': '天津市', '130000': '河北省', ...}

Data['130000']
// 对应省份的所有城市：{'130100': '石家庄市', '130200': '唐山市', '130300': '秦皇岛市', ...}

Data['130200']
// 对应市的所有县区：{'130201': '市辖区', '130202': '路南区', '130203': '路北区', ...}
```
