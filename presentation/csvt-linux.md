# CSVT Linux 研習
---
5th 張智仁(繁嵐)

---

## 通往異世界的入口: VirtualBox
* Virtual Machine
* Easy to use
* NOT open source completely

--

### 初始設定
* 新增機器
* EFI 開機模式
* CPU 上限
* 安裝媒介*(.iso)*

---

## 安裝 Linux

--

#### 下一步、下一步、下一步......

--

### 設定登入帳密
* 然後下一步

---

## 漫長的等待......

---

## Linux 是什麼，能吃嗎?

---

### Operating System
* system program
* manage hardware and application

--

### 常見的作業系統
* Windows
* Linux
* MacOS

<br>
<img height="100" src="https://upload.wikimedia.org/wikipedia/commons/b/b0/NewTux.svg">
<h6>Photo credit: lewing@isc.tamu.edu Larry Ewing and The GIMP</h6>

---

### Linux (Kernel)
* Created by Linus Torvalds
* **Open Source**

--

### Linux distribution
* Kernel + 其他打包好的軟體
* 主要差異可能會是套件管理、圖形介面
* 發行版派系
  * Debian
  * Redhat
  * Arch
  * Android

<br>
<img height="100" src="https://www.debian.org/logos/openlogo.svg">
<img height="100" src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Fedora_logo.svg">
<img height="100" src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Archlinux-icon-crystal-64.svg">

--

<img height="100" src="https://upload.wikimedia.org/wikipedia/commons/9/9d/Ubuntu_logo.svg">

* 基於 Debian 開發
* 主要由 Canonical 公司維護
* 商業發行版

---

## 學習詠唱咒語
#### Linux 指令的使用
與 Linux 溝通的第一步

---

## Terminal 終端機
* 純文字介面
* 用來存取 Shell

--

### 開啟終端機
* Ctrl+Shift+T
* 系統選單->系統工具->終端機

---

## 常用的 Linux 指令

--

### `pwd`
* *print working directory*
* 顯示目前你所在的位置

--

### `ls`
* *list*
* 列出資料夾裡的內容
* 預設列出你目前所在的資料夾

```bash
ls
ls <資料夾名稱>
ls -a # 列出隱藏內容
ls -l # 列出詳細資料
```

--

### `cd`
* *change directory*
* 切換資料夾

```bash
cd <資料夾名稱>
```

---

### 插播: 位置表示法

--

#### 絕對位置
##### 宇宙銀河系太陽系地球台灣彰化縣彰化市中興路78號的資訊館
* 以 / 開頭

--

#### 相對位置
##### 彰中操場的旁邊
* 不以 / 開頭
* *.* 開頭: 目前所在的位置
* *..* 開頭: 目前所在的位置的上一層

---

## 中場練習
* 嘗試顯示你目前的資料夾位置
* 列出目前資料夾的內容
* 切換到上一層資料夾，再切換回去

---

### `mkdir`
* *make directory*
* 建立資料夾

```bash
mkdir <新資料夾名稱>
```

--

### `cat`
* ~~貓~~ *concatenate*
* 檢視檔案內容

```bash
cat <檔案名稱>
```

---

<section data-background-image="https://media.giphy.com/media/XUFPGrX5Zis6Y/giphy.gif" data-background-transition="none">
  <h2>毀滅性法術</h2>
  <h4>具有風險的指令們</h4>
  <p>請小心使用!</p>
</section>
<section data-background-color="rgb(200,128,128)" data-background-transition="none">
  <h3><code>mv</code></h3>
  <ul>
    <li><i>move</i></li>
    <li>移動檔案或資料夾</li>
    <li>更改名稱</li>
    <li><b>覆蓋檔案</b></li>
  </ul>
  <pre><code data-trim data-noescape>
    mv <檔案名稱> <資料夾名稱>
    mv <原名稱> <新名稱>
  </code></pre>
</section>
<section data-background-color="rgb(200,96,96)" data-background-transition="none">
  <h3><code>rm</code></h3>
  <ul>
    <li><i>remove</i></li>
    <li>刪除檔案或資料夾</li>
    <li><b>不可逆</b></li>
  </ul>
  <pre><code data-trim data-noescape>
    rm <檔案名稱>
    rm -R <資料夾名稱>
  </code></pre>
</section>
<section data-background-color="rgb(200,128,128)" data-background-transition="none">
  <h3><code>sudo</code></h3>
  <ul>
    <li><i>superuser do</i></li>
    <li>以管理員權限執行</li>
  </ul>
  <pre><code data-trim data-noescape>
    sudo <指令>
  </code></pre>
</section>

---

## 中場練習
* 建立 `test` 資料夾
* 將 `test` 資料夾重命名為 `byebye`
* 刪除 `byebye` 資料夾

---

## Bonus: 權限控制
### *如果還有時間的話*

--

### Linux 檔案系統權限
* user, group, others
* 擁有者、擁有的群組、其他人們
* 這三個可簡稱為 *all*

--

* 讀取、寫入、執行
* **r**ead, **w**rite, e**x**ecute

--

還記得`ls -l`嗎?
* \- \--- \--- \---
* 類型 \ user \ group \ others

--

### `chown`
* *change owner*
* 變更擁有者

```bash
chown <群組名>:<使用者名> <檔案或資料夾名稱>
```

--

### `chmod`
* *change mode*
* 改變資料權限
* 數字型
  * 三位數
  * read: 4
  * write: 2
  * execute: 1
* 字母型
  * +, -, =
  * r, w, x

```bash
chmod <數字或字母> <檔案或資料夾名稱>
```

---

## 突破結界: 遠端連線
透過 SSH

--

### SSH
* 出門在外使用
* 本體是一個協定 (like HTTP, FTP)

--

### 開始使用
* 透過內建終端機
```bash
ssh 使用者名稱@IP
```

* 透過 Putty

![](https://upload.wikimedia.org/wikipedia/commons/b/b6/PuTTY_icon_128px.png)

--

### 連線成功!
* 可以像原本使用終端機那樣進行操作

---

## Q&A

