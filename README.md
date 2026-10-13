# 城南市场 · 摊位运营台（微信渐进 3D）

不砍三维、不砍摊位功能。首屏先出台账/搜索/平面图，后台加载 Draco 压缩 GLB。

## 本地开发

```bash
npm i
npm run dev    # http://127.0.0.1:4178/
npm run build
npm run preview
```

## 微信验证

1. 部署到 HTTPS（GitHub Pages）。
2. 微信内打开链接。
3. 首屏应立刻能搜 `D1-27` / `A2-55` 并打开档案改租金。
4. 底部出现「三维加载」进度，完成后可揭顶（外观 / 揭顶·一层 / 二层）。

## 体积（约）

| 资源 | raw | 说明 |
|---|---:|---|
| 首屏 JS+CSS | ~60KB | 可交互 |
| stalls.json | 444KB（gzip ~24KB） | 台账 |
| three chunk | ~595KB（gzip ~152KB） | 延后 |
| mobile_draco.glb | 1.5MB | 微信默认 |
| desktop_draco.glb | 1.7MB | 桌面默认 |

旧单文件 monolith ≈ 9.7MB 一次吞完。
