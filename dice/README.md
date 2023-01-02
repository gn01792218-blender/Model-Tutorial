# Dice 一般模式建模步驟提示 : 
## 1.將Cube 製作出 5*5 的切割線
## 2.挖洞
選好要挖洞的格子
### (1)使用快捷鍵i內縮
### (2)使用poke faces功能戳洞 : 
```
ctrl+F --> Poke Faces 
```
此功能，如字面上意思，戳面<br>
我們可以透過設置Poke Offset 的數值，來看要戳像裡面還是外面(數值正向外；數值負向內)

## 3.使用表面細分修改器 
## 4.Shade Smooth 做最後收尾

# Dice Geometry Nodes 模式建模步驟

## 1.切割cube為5*5，並且平滑處理 
 (1)增加一個Subdivide Mesh 節點 ( 只會切分出更多頂點 )<br>
 (2)增加一個Subdivision Surface 節點 ( 表面細分，會執行平滑工作smooth )
 (3)增加一個Set Shade Smooth 節點 ( 光滑處理 )
## 2.挖洞


## 教學影片
https://www.udemy.com/course/blender-environments/learn/lecture/32846858#overview

# 作業檢核目標 : 
1.物件名稱是否有取好
2.是否有將場景中的物件做好分類

