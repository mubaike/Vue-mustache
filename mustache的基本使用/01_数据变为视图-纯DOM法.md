```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="list"></div>
    <script>
        var arr = [
            {"name": "小明", "age": 12, "sex": "男"},
            {"name": "小红", "age": 12, "sex": "女"},
            {"name": "小强", "age": 12, "sex": "男"}
        ];

        var list = document.getElementById('list');
        
        for (let i = 0; i < arr.length; i++) {
            //每遍历一项，都要用DOM方法去创建li标签
            let oLi = document.createElement('li');
            //创建hd这个div
            let hdDiv = document.createElement('div');
            hdDiv.className = 'hd';
            hdDiv.innerText = arr[i].name + '的基本信息';

            //创建的节点是孤儿节点，所以必须要上树才能被用户看见
            oLi.appendChild(hdDiv);
            //创建的节点是孤儿节点，所以必须要上树才能被用户看见
            list.appendChild(oLi);
        }
    </script>
</body>
</html>
```
