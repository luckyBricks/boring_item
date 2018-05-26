# 工作进度条

## 使用方法：

将 pypg.py 放置你的项目相同路径下

```
from pypg import PyProgress

total = 150
p = PyProgress(total, isIpy=True)
for i in range(total+1):
        time.sleep(0.1)
        p.update(i)
```

## 实际应用

```
pg = PyProgress(len(data), delay=0)
    for k, row in enumerate(data):
        content_url = row[3]
        content = get_content(content_url)
        if not content:
            print('failed connect url: {}'.format(content_url))
        row.append(content)
        pg.update(k)
```

## 运行结果：
![运行结果](src/0.png)