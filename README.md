<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>前端学习示例页面</title>
    <style>
        /* 基础样式重置 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: "Microsoft YaHei", sans-serif;
            background-color: #f0f2f5;
            color: #333;
            line-height: 1.6;
        }

        /* 头部区域 */
        header {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        /* 主内容区域 */
        .container {
            max-width: 1000px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        .card {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            padding: 2rem;
            margin-bottom: 2rem;
        }

        .card h2 {
            color: #2c3e50;
            border-left: 4px solid #3498db;
            padding-left: 1rem;
            margin-bottom: 1rem;
        }

        .code-example {
            background-color: #f8f9fa;
            border: 1px solid #e9ecef;
            border-radius: 4px;
            padding: 1rem;
            margin: 1rem 0;
            font-family: Consolas, monospace;
            font-size: 0.9rem;
            overflow-x: auto;
        }

        /* 按钮样式 */
        .btn {
            display: inline-block;
            background-color: #3498db;
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            text-decoration: none;
            transition: background-color 0.3s;
        }

        .btn:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>
    <header>
        <h1>前端学习示例页面</h1>
        <p>HTML + CSS 入门练习</p>
    </header>

    <div class="container">
        <div class="card">
            <h2>什么是前端？</h2>
            <p>前端开发主要负责网页的界面与交互，核心技术栈包括：</p>
            <ul>
                <li><strong>HTML</strong>：定义网页的结构和内容</li>
                <li><strong>CSS</strong>：控制网页的样式和布局</li>
                <li><strong>JavaScript</strong>：实现网页的交互逻辑</li>
            </ul>
        </div>

        <div class="card">
            <h2>HTML 示例</h2>
            <p>这是一个最基础的 HTML 文档结构：</p>
            <div class="code-example">
&lt;!DOCTYPE html&gt;<br>
&lt;html&gt;<br>
&nbsp;&nbsp;&lt;head&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;meta charset="UTF-8"&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;我的第一个页面&lt;/title&gt;<br>
&nbsp;&nbsp;&lt;/head&gt;<br>
&nbsp;&nbsp;&lt;body&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;h1&gt;Hello, World!&lt;/h1&gt;<br>
&nbsp;&nbsp;&lt;/body&gt;<br>
&lt;/html&gt;
            </div>
        </div>

        <div class="card">
            <h2>点击按钮试试</h2>
            <button class="btn" onclick="alert('你点击了按钮！')">点我有惊喜</button>
        </div>
    </div>
</body>
</html>
