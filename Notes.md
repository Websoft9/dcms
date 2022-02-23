# DCMS

数据驱动的CMS，维护网站就像操作 Excel 一样简单。

## 驱动力

当前的 CMS，提供了“丰富的后台”，让用户在后台通过可视化的方式创作网站，用户也通过这种方式可以创作网站出来。  
但是，站在CEO的角度，企业的网站仅用作介绍公司，而无法作为内容营销的载体。  

DCMS 是以内容营销建模为核心，再结合与数据有关的展示模板，帮助用户快速建议一个具有**内容营销最佳实践**网站。

这个是产品的原生驱动力。

## 架构

* 无代码平台/Headless/数据库  承载数据库模型
* Graph 中间件与前端集成
* 构建出100%的前端代码供用户部署
* 提供一套 SaaS 生产平台
* 发布与生产脱离


## 问题

#### 多语言怎么处理？

咨询了 supabase 的大神，得到其[回复](https://github.com/supabase/supabase/issues/5561)如下

```
create another column. eg if you had post, you might create post_en to store english
create a JSONB column with unstructured data. eg, if you had post you might create post_i18n to store all translations
create a translations table. eg, if you had a table posts, you might create a table posts_i18n and store all the translations in that table
```
