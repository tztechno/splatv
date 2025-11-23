```
index.html + hybrid.js + model.splatv


hybrid.js 2025/11/23
L.873


// 花火設定: 6.28秒サイクル、最後の2秒を待機時間に
let cycle_duration = 6.28;  // 秒
let firework_duration = 4.28;  // 花火表示時間（秒）
let elapsed = (Date.now() / 1000) % cycle_duration;
let t;
if (elapsed < firework_duration) {
    t = elapsed / firework_duration;  // 0.0 → 1.0（花火）
} else {
    t = 1.0;  // 待機中（消えた状態）
}
gl.uniform1f(u_time, t);
// 花火設定: 6.28秒サイクル、最後の2秒を待機時間に 


gl.uniform1f(u_time, (Date.now() / 6280) % 1.0); //1方向 for hanabi


gl.uniform1f(u_time, Math.sin(Date.now() / 1000) / 2 + 1 / 2); //往復,original


```
