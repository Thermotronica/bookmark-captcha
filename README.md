# bookmark-captcha
♥️
click below ...

[View CMYK Droplet](data:text/html;charset=utf-8,%3C!DOCTYPE%20html%3E%3Chtml%3E%3Chead%3E%3Cmeta%20charset=%22UTF-8%22%3E%3Ctitle%3ECMYK%20Droplet%3C/title%3E%3C/head%3E%3Cbody%20style=%22margin:0;overflow:hidden;background:%23000;%22%3E%3Ccanvas%20id=%22c%22%3E%3C/canvas%3E%3Cscript%20type=%22x-shader/x-fragment%22%20id=%22frag%22%3Eprecision%20mediump%20float;uniform%20float%20u_time;uniform%20vec2%20u_res;vec3%20cmykToRgb(vec4%20cmyk)%7Bfloat%20r=(1.0-cmyk.x)(1.0-cmyk.w);float%20g=(1.0-cmyk.y)(1.0-cmyk.w);float%20b=(1.0-cmyk.z)(1.0-cmyk.w);return%20vec3(r,g,b);%7Dvoid%20main()%7Bvec2%20uv=gl_FragCoord.xy/u_res.xy;uv-=0.5;uv.x=u_res.x/u_res.y;float%20t=u_time0.2;float%20d=length(uv);float%20ripple=sin(d40.0-t10.0)0.02;uv+=normalize(uv)ripple;float%20c=0.5+0.5sin(t);float%20m=0.5+0.5sin(t+2.0);float%20y=0.5+0.5sin(t+4.0);float%20k=0.2+0.2sin(t+6.0);vec3%20color=cmykToRgb(vec4(c,m,y,k));float%20vignette=smoothstep(0.8,0.0,d);color=vignette;gl_FragColor=vec4(color,1.0);%7D%3C/script%3E%3Cscript%20type=%22x-shader/x-vertex%22%20id=%22vert%22%3Eattribute%20vec2%20a_position;void%20main()%7Bgl_Position=vec4(a_position,0.0,1.0);%7D%3C/script%3E%3Cscript%3Econst%20canvas=document.getElementById('c');const%20gl=canvas.getContext('webgl');canvas.width=innerWidth;canvas.height=innerHeight;function%20createShader(t,s)%7Bconst%20h=gl.createShader(t);gl.shaderSource(h,s);gl.compileShader(h);return%20h;%7Dconst%20vert=createShader(gl.VERTEX_SHADER,document.getElementById('vert').textContent);const%20frag=createShader(gl.FRAGMENT_SHADER,document.getElementById('frag').textContent);const%20prog=gl.createProgram();gl.attachShader(prog,vert);gl.attachShader(prog,frag);gl.linkProgram(prog);gl.useProgram(prog);const%20buf=gl.createBuffer();gl.bindBuffer(gl.ARRAY_BUFFER,buf);gl.bufferData(gl.ARRAY_BUFFER,new%20Float32Array(%5B-1,-1,1,-1,-1,1,1,-1,1,1,-1,1%5D),gl.STATIC_DRAW);const%20pos=gl.getAttribLocation(prog,'a_position');gl.enableVertexAttribArray(pos);gl.vertexAttribPointer(pos,2,gl.FLOAT,false,0,0);const%20ut=gl.getUniformLocation(prog,'u_time');const%20ur=gl.getUniformLocation(prog,'u_res');function%20draw(t)%7Bgl.viewport(0,0,canvas.width,canvas.height);gl.uniform1f(ut,t*0.001);gl.uniform2f(ur,canvas.width,canvas.height);gl.drawArrays(gl.TRIANGLES,0,6);requestAnimationFrame(draw);%7DrequestAnimationFrame(draw);%3C/script%3E%3C/body%3E%3C/html%3E)

you can also create an HTML file with the following content and open it in your browser to see the artifact:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>CMYK Droplet</title>
</head>
<body style="margin:0;overflow:hidden;background:#000;">
    <canvas id="c"></canvas>
    <script type="x-shader/x-fragment" id="frag">
        precision mediump float;
        uniform float u_time;
        uniform vec2 u_res;
        vec3 cmykToRgb(vec4 cmyk) {
            float r = (1.0 - cmyk.x) * (1.0 - cmyk.w);
            float g = (1.0 - cmyk.y) * (1.0 - cmyk.w);
            float b = (1.0 - cmyk.z) * (1.0 - cmyk.w);
            return vec3(r, g, b);
        }
        void main() {
            vec2 uv = gl_FragCoord.xy / u_res.xy;
            uv -= 0.5;
            uv.x *= u_res.x / u_res.y;
            float t = u_time * 0.2;
            float d = length(uv);
            float ripple = sin(d * 40.0 - t * 10.0) * 0.02;
            uv += normalize(uv) * ripple;
            float c = 0.5 + 0.5 * sin(t);
            float m = 0.5 + 0.5 * sin(t + 2.0);
            float y = 0.5 + 0.5 * sin(t + 4.0);
            float k = 0.2 + 0.2 * sin(t + 6.0);
            vec3 color = cmykToRgb(vec4(c, m, y, k));
            float vignette = smoothstep(0.8, 0.0, d);
            color *= vignette;
            gl_FragColor = vec4(color, 1.0);
        }
    </script>
    <script type="x-shader/x-vertex" id="vert">
        attribute vec2 a_position;
        void main() {
            gl_Position = vec4(a_position, 0.0, 1.0);
        }
    </script>
    <script>
        const canvas = document.getElementById('c');
        const gl = canvas.getContext('webgl');
        canvas.width = innerWidth;
        canvas.height = innerHeight;
        function createShader(t, s) {
            const h = gl.createShader(t);
            gl.shaderSource(h, s);
            gl.compileShader(h);
            return h;
        }
        const vert = createShader(gl.VERTEX_SHADER, document.getElementById('vert').textContent);
        const frag = createShader(gl.FRAGMENT_SHADER, document.getElementById('frag').textContent);
        const prog = gl.createProgram();
        gl.attachShader(prog, vert);
        gl.attachShader(prog, frag);
        gl.linkProgram(prog);
        gl.useProgram(prog);
        const buf = gl.createBuffer();
        gl.bindBuffer(gl.ARRAY_BUFFER, buf);
        gl.bufferData(gl.ARRAY_BUFFER, new Float32Array([-1, -1, 1, -1, -1, 1, 1, -1, 1, 1, -1, 1]), gl.STATIC_DRAW);
        const pos = gl.getAttribLocation(prog, 'a_position');
        gl.enableVertexAttribArray(pos);
        gl.vertexAttribPointer(pos, 2, gl.FLOAT, false, 0, 0);
        const ut = gl.getUniformLocation(prog, 'u_time');
        const ur = gl.getUniformLocation(prog, 'u_res');
        function draw(t) {
            gl.viewport(0, 0, canvas.width, canvas.height);
            gl.uniform1f(ut, t * 0.001);
            gl.uniform2f(ur, canvas.width, canvas.height);
            gl.drawArrays(gl.TRIANGLES, 0, 6);
            requestAnimationFrame(draw);
        }
        requestAnimationFrame(draw);
    </script>
</body>
</html>
```
