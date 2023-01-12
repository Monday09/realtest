<!DOCTYPE html>
<html lang="en">
    
<head>
    <title>Document</title>
    <link rel = "stylesheet" href= "ani.css">    
</head>

<body>
    <style>
        body
        {
            background-color: black;
            height: 5000px;
            font-family: 'nanumsquare';
        }

        div
        {
            margin-top: 1000px;
            color: white;
            text-align: center;
            opacity: 0;
            transition: all 0.5s;
        }
    </style>

    <div><h1>안녕하세요</h1></div>
    <div><h1>감사해요</h1></div>
    <div><h1>잘있어요</h1></div>
    <div><h1>다시만나요</h1></div>

    <!-- script -->
    <script>
        let observer = new IntersectionObserver((e) => {
            e.forEach((box) => {
                if(box.isIntersecting) {
                    box.target.style.opacity = 15;
                }
                else {
                    box.target.style.opacity = 0;
                }
            })
        })

        let div = document.querySelectorAll('div')
        observer.observe(div[0])
        observer.observe(div[1])
        observer.observe(div[2])
        observer.observe(div[3])

    </script>
</body>
</html>
