- remove jme部分
- 修改部分代码，可设置一个basepath，可从任意指定basepath目录下加载，如下所示
```JAVA
	Globals globals = JsePlatform.standardGlobals(xxx);
```
本来框架内遇到lua的require代码时候
```lua
require (xxx)
```
会以java的`getResourceAsStream`去找文件，这就要求了lua文件必须和.class保持一个相对路径的关联。但我更想要的方式是java方面打包成一个jar和lua无关，所以稍微修改了一下框架。
