<<<<<<< HEAD
## ❤️爱心代码集合

### 🤩使用方法

#### 💌本地使用
将 **html** 代码文件下载至本地，并使用浏览器打开

#### 💌在线预览
- HTML代码点击网址即可在线预览效果

注意：在`电脑端`显示效果最佳，手机端可能无法正常显示

|   文件   |   网页效果   | 说明  |
| ---- | ---- |---- |
|   love.html   |   [http://huawuque404.com/love-code/love.html](http://huawuque404.com/love-code/love.html)   | 爱心代码初版 |
|   love-add.html   |   [http://huawuque404.com/love-code/love-add.html](http://huawuque404.com/love-code/love-add.html)   | 在爱心中增加了文字 |
|   love2.html   |   [http://huawuque404.com/love-code/love2.html](http://huawuque404.com/love-code/love2.html)   |  点击屏幕爱心飞屏效果  |
| love-add2.html | [http://huawuque404.com/love-code/love-add2.html](http://huawuque404.com/love-code/love-add2.html) | 添加背景图片 |
| love-add3.html | [http://huawuque404.com/love-code/love-add3.html](http://huawuque404.com/love-code/love-add3.html) | 爱心代码跳动效果 |
| love3.html | [http://huawuque404.com/love-code/love3.html](http://huawuque404.com/love-code/love3.html) | 文字满屏漂浮效果 |
| love4.html | [http://huawuque404.com/love-code/love4.html](http://huawuque404.com/love-code/love4.html) | 文字随机掉落炫酷黑客代码效果 |
| 流星雨.html | [http://huawuque404.com/love-code/stars.html](http://huawuque404.com/love-code/stars.html) | 流星雨效果 |
| 星空特效.html | [http://huawuque404.com/love-code/star.html](http://huawuque404.com/love-code/star.html) | 星空旋转效果 |
| --- | --- | --- |

- 其它语言代码下载或者复制在相应编译器中运行查看效果

欢迎大家一起来创造更多好看的爱心效果！🍉

### 👨‍💻代码规范
- 如果要增加更多好看的爱心代码，则 PR 时 HTML 文件以 love2 、love3 、love4 依次命名，如果有对应的独立 CSS 和 JavaScript 文件，则命名为 love2.css 和 love2.js 。一种效果如果有多个代码文件则统一放在一个文件夹中，例如 love2.html，love2.css，love2.js 放在文件夹 love2 中
- 如果是增加功能，可以重写代码合并。但是更推荐采用保留原文件，新增一个`原文件名-add`的文件的方式。例如首先有一个 love.html 文件，新增代码则新建一个 love-add.html 文件，增加第二次功能则新建一个 love-add2.html 文件

> 以上代码收集于互联网开源代码，只作为兴趣爱好收集，不作任何商业用途，如有侵权，请告知删除

### 联系我

#### 📢博客：[https://blog.csdn.net/coder_heweilai](https://blog.csdn.net/coder_heweilai)

#### 🍊微信：

加好友备注`github`

![微信号_243x239](https://user-images.githubusercontent.com/109327586/204129722-898d481f-1735-452f-8a60-9bf298dc5bce.png)


=======
<!DOCTYPE html>
<html>

<head>
    <title> 爱心代码 </title>
    <meta charset="utf-8">
    <meta name="Author" content="花无缺">
    <meta name="Keywords" content="爱心代码">
    <meta name="Description" content="爱心代码">
    <link rel="shortcut icon" href="../picture/爱心.png" type="image/x-icon">
    <style>
        html,
        body {
            height: 100%;
            padding: 0;
            margin: 0;
            background: #000;
        }

        canvas {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .title {
            width: 20%;
            height: 30%;
            /* 文字居中 */
            text-align: center;
            /* 字体大小 */
            font-size: 30px;
            /* 背景颜色 */
            background-color: transparent;
            /* 文字颜色 */
            color: rgba(247, 110, 206, 0.829);
            /* 左右居中 */
            margin: auto;
            /* 定位 */
            position: relative;
            /* 上边距 */
            top: 40%;
            /* 字体 */
            font-family: "幼圆";
        }
    </style>

</head>

<body>


    <canvas id="pinkboard"></canvas>

    <div class="title">花无缺，我喜欢你</div>
    <script>

        var settings = {
            particles: {
                length: 500,
                duration: 2,
                velocity: 100,
                effect: -0.75,
                size: 30,
            },
        };


        (function () { var b = 0; var c = ["ms", "moz", "webkit", "o"]; for (var a = 0; a < c.length && !window.requestAnimationFrame; ++a) { window.requestAnimationFrame = window[c[a] + "RequestAnimationFrame"]; window.cancelAnimationFrame = window[c[a] + "CancelAnimationFrame"] || window[c[a] + "CancelRequestAnimationFrame"] } if (!window.requestAnimationFrame) { window.requestAnimationFrame = function (h, e) { var d = new Date().getTime(); var f = Math.max(0, 16 - (d - b)); var g = window.setTimeout(function () { h(d + f) }, f); b = d + f; return g } } if (!window.cancelAnimationFrame) { window.cancelAnimationFrame = function (d) { clearTimeout(d) } } }());


        var Point = (function () {
            function Point(x, y) {
                this.x = (typeof x !== 'undefined') ? x : 0;
                this.y = (typeof y !== 'undefined') ? y : 0;
            }
            Point.prototype.clone = function () {
                return new Point(this.x, this.y);
            };
            Point.prototype.length = function (length) {
                if (typeof length == 'undefined')
                    return Math.sqrt(this.x * this.x + this.y * this.y);
                this.normalize();
                this.x *= length;
                this.y *= length;
                return this;
            };
            Point.prototype.normalize = function () {
                var length = this.length();
                this.x /= length;
                this.y /= length;
                return this;
            };
            return Point;
        })();


        var Particle = (function () {
            function Particle() {
                this.position = new Point();
                this.velocity = new Point();
                this.acceleration = new Point();
                this.age = 0;
            }
            Particle.prototype.initialize = function (x, y, dx, dy) {
                this.position.x = x;
                this.position.y = y;
                this.velocity.x = dx;
                this.velocity.y = dy;
                this.acceleration.x = dx * settings.particles.effect;
                this.acceleration.y = dy * settings.particles.effect;
                this.age = 0;
            };
            Particle.prototype.update = function (deltaTime) {
                this.position.x += this.velocity.x * deltaTime;
                this.position.y += this.velocity.y * deltaTime;
                this.velocity.x += this.acceleration.x * deltaTime;
                this.velocity.y += this.acceleration.y * deltaTime;
                this.age += deltaTime;
            };
            Particle.prototype.draw = function (context, image) {
                function ease(t) {
                    return (--t) * t * t + 1;
                }
                var size = image.width * ease(this.age / settings.particles.duration);
                context.globalAlpha = 1 - this.age / settings.particles.duration;
                context.drawImage(image, this.position.x - size / 2, this.position.y - size / 2, size, size);
            };
            return Particle;
        })();


        var ParticlePool = (function () {
            var particles,
                firstActive = 0,
                firstFree = 0,
                duration = settings.particles.duration;

            function ParticlePool(length) {
                // create and populate particle pool
                particles = new Array(length);
                for (var i = 0; i < particles.length; i++)
                    particles[i] = new Particle();
            }
            ParticlePool.prototype.add = function (x, y, dx, dy) {
                particles[firstFree].initialize(x, y, dx, dy);

                // handle circular queue
                firstFree++;
                if (firstFree == particles.length) firstFree = 0;
                if (firstActive == firstFree) firstActive++;
                if (firstActive == particles.length) firstActive = 0;
            };
            ParticlePool.prototype.update = function (deltaTime) {
                var i;


                if (firstActive < firstFree) {
                    for (i = firstActive; i < firstFree; i++)
                        particles[i].update(deltaTime);
                }
                if (firstFree < firstActive) {
                    for (i = firstActive; i < particles.length; i++)
                        particles[i].update(deltaTime);
                    for (i = 0; i < firstFree; i++)
                        particles[i].update(deltaTime);
                }


                while (particles[firstActive].age >= duration && firstActive != firstFree) {
                    firstActive++;
                    if (firstActive == particles.length) firstActive = 0;
                }


            };
            ParticlePool.prototype.draw = function (context, image) {

                if (firstActive < firstFree) {
                    for (i = firstActive; i < firstFree; i++)
                        particles[i].draw(context, image);
                }
                if (firstFree < firstActive) {
                    for (i = firstActive; i < particles.length; i++)
                        particles[i].draw(context, image);
                    for (i = 0; i < firstFree; i++)
                        particles[i].draw(context, image);
                }
            };
            return ParticlePool;
        })();


        (function (canvas) {
            var context = canvas.getContext('2d'),
                particles = new ParticlePool(settings.particles.length),
                particleRate = settings.particles.length / settings.particles.duration,
                time;


            function pointOnHeart(t) {
                return new Point(
                    160 * Math.pow(Math.sin(t), 3),
                    130 * Math.cos(t) - 50 * Math.cos(2 * t) - 20 * Math.cos(3 * t) - 10 * Math.cos(4 * t) + 25
                );
            }


            var image = (function () {
                var canvas = document.createElement('canvas'),
                    context = canvas.getContext('2d');
                canvas.width = settings.particles.size;
                canvas.height = settings.particles.size;

                function to(t) {
                    var point = pointOnHeart(t);
                    point.x = settings.particles.size / 2 + point.x * settings.particles.size / 350;
                    point.y = settings.particles.size / 2 - point.y * settings.particles.size / 350;
                    return point;
                }

                context.beginPath();
                var t = -Math.PI;
                var point = to(t);
                context.moveTo(point.x, point.y);
                while (t < Math.PI) {
                    t += 0.01;
                    point = to(t);
                    context.lineTo(point.x, point.y);
                }
                context.closePath();

                context.fillStyle = '#ea80b0';
                context.fill();

                var image = new Image();
                image.src = canvas.toDataURL();
                return image;
            })();


            function render() {

                requestAnimationFrame(render);


                var newTime = new Date().getTime() / 1000,
                    deltaTime = newTime - (time || newTime);
                time = newTime;


                context.clearRect(0, 0, canvas.width, canvas.height);


                var amount = particleRate * deltaTime;
                for (var i = 0; i < amount; i++) {
                    var pos = pointOnHeart(Math.PI - 2 * Math.PI * Math.random());
                    var dir = pos.clone().length(settings.particles.velocity);
                    particles.add(canvas.width / 2 + pos.x, canvas.height / 2 - pos.y, dir.x, -dir.y);
                }


                particles.update(deltaTime);
                particles.draw(context, image);
            }


            function onResize() {
                canvas.width = canvas.clientWidth;
                canvas.height = canvas.clientHeight;
            }
            window.onresize = onResize;


            setTimeout(function () {
                onResize();
                render();
            }, 10);
        })(document.getElementById('pinkboard'));
    </script>



</body>

</html>
>>>>>>> 6c3101d87a3e9c12e87e201cc01d385bc2b7a852
