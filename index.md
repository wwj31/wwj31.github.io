## 王文杰的主页
游戏行业，不想加班的后端



#### 笔记
json官方库，值类型是[]byte的一个细节:
```go
func ExampleJson() {
	m := make(map[string]interface{})
	// String values encode as JSON strings coerced to valid UTF-8,
	// replacing invalid bytes with the Unicode replacement rune.
	m["key1"] = "this is example"

	// []byte encodes as a base64-encoded string, and a nil slice
	// encodes as the null JSON value.
	m["key2"] = []byte("this is example")
	
	ret, _ := json.Marshal(m)
	fmt.Println(string(ret))
	
	// map存储的[]byte类型，序列化会被编码成base64
	
	// OutPut:{"key1":"this is example","key2":"dGhpcyBpcyBleGFtcGxl"}
}
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/wwj31/wwj31.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
