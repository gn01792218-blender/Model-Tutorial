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
主要概念是透過Boolean節點來做裁切、挖洞效果；然後我們要挖的洞是圓形<br>
 (1)增加一個Mesh Boolean : <br>
    其內有兩個Mesh可以輸入( 一個作為要被裁切的Mesh，一個做為裁切Mesh )<br>
    所先將骰子本體連接到Mesh1
 (2)增加一個UV Sphere ，搭配Transform、Subdivision Surface、Set Shade Smooth節點 : <br>
    用來告訴Boolean要切出圓形，並且要切在哪裡(透過Transform調整位置)，
    透過Location調整洞洞的位置，並且使用Rotation來調整球體旋轉方向
 (3)重複執行以上1、2切出所有洞

## 3.修復洞洞奇怪的邊緣
使用修改器-Edge Split來修復就可以了( 目前Geometry Nodes 中沒有這個修改器節點可以使用 )

## PS.為節點添加不同的顏色
由於視窗終將會有很多節點，所以我們可以透過給節點不一樣的顏色，來方便管理<br>
對著該節點，按下N，開啟節點N面板，勾選Color，就可以設置Color


## 教學影片
https://www.udemy.com/course/blender-environments/learn/lecture/32846858#overview

# 作業檢核目標 : 
1.物件名稱是否有取好
2.是否有將場景中的物件做好分類

