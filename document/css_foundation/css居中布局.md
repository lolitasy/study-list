# CSS居中布局 #
相信大家肯定知道css的居中布局
下面我来总结一下总共有哪些布局方式

        div
        <div class="parent">
            <div class="child">DOME</div>
        </div>
### 水平居中

1.父级用text-align : center
  子级用display : inline-block

        css
        .parent{
            text-align: center;
            background: #023232;
        }
        .child{
            display: inline-block;
            background: #f34343;
        }

2.table+margin

        css
        .child{
            display: table;
            background: #f34343;
            margin: 0 auto;
        }

3.absolute + transform

        css
        .parent{
            position: relative;
        }
        .child{
            position: absolute;
            background: #f34343;
            left: 50%;
            transform: translateX(-50%);
        }

4.flex+justify-content

        css 
        .parent{ 
            display: flex;
            justify-content: center;
        }

5.flex+margin

        css 
        .parent{ 
            display: flex;
        }
        .child{
            magin:0 auto;
        }

6.absolute+margin 必须定宽定高

        .parent {
            position: relative;
            width: 500px;
            height: 500px;
        }
        .child {
            position: absolute;
            left: 0;
            right: 0;
            margin: auto;
            width: 100px;
            height: 100px;
        }

7.absolute  必须定宽定高

        .parent {
            position: relative;
            width: 500px;
        }
        .child{
            position: absolute;
            left: 50%;
            margin-left: -250%;
        }
### 垂直居中
    
1.table-cell+vertical-align

        css 
        .parent{ 
            display: table-cell;
            vertical-align: middle;
            height: 500px;
        }

2.absolute+transform

        .parent{
            position: relative;
            height: 500px;
        }
        .child{
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
        }
 
 3.flex+align-items: center;

        .parent{
            display: flex;
            background: red;
            height: 500px;
            align-items: center;
        }
        .child{
            background: yellow;
        }

4.position:absolute

        .parent {
            position: relative;
            width: 100px;
            height: 100px;
        }
        .child {
            position: absolute;
            top: 50%;
            margin-top: -10px;
            height: 20px;
        }

### 水平垂直布局

1.表格布局

        .parent{
            display: table-cell;
            text-align: center;
            vertical-align: middle;
        }
        .child{
            display: inline-block;
        }

2.transform+absolute

        .parent{
            position: relative;
        }
        .child{
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%,-50%);
        }
3.flex布局

        .parent{
            display: flex;
            justify-content: center;
            align-items: center;
        }

4.absolute+margin 必须定宽定高

        .parent {
            position: relative;
            width: 500px;
            height: 500px;
        }
        .child {
            position: absolute;
            left: 0;
            right: 0;
            top:0;
            bottom:0;
            margin: auto;
            width: 100px;
            height: 100px;
        }

5.left+margin+absolute  必须定宽定高

        .parent {
            position: relative;
            width: 500px;
            height: 500px;
        }
        .child {
            position: absolute;
            width: 100px;
            height: 100px;
            top: 50%;
            left: 50%;
            margin-top: -50px;
            margin-left: -50px;
        }
