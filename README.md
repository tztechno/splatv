```
index.html + hybrid.js + model.splatv


hybrid.js 2025/11/23
L.873
gl.uniform1f(u_time, (Date.now() / 6280) % 1.0); //1方向 for hanabi
gl.uniform1f(u_time, Math.sin(Date.now() / 1000) / 2 + 1 / 2); //往復
```
