# 3D Mobile Game

2024/03/10 嘉義高商 - Unity 移動平台遊戲課程

## 課程簡介

這是一個 Unity 教學專案，我們會用一款已經做好基礎功能的 3D 俯視角生存射擊遊戲，帶你學會如何在移動平台上開發遊戲，包含觸控搖桿、敵人生成、武器系統與打包發佈到 Android。

## 玩法與操作

| 輸入方式 | 動作 |
|----------|------|
| 左側虛擬搖桿 | 移動角色 |
| 右側虛擬搖桿 | 控制角色面向 |
| W / A / S / D | 移動角色（測試用） |
| 滑鼠指向 | 瞄準方向（測試用） |

遊戲目標：操控角色在場地中存活，自動射擊消滅不斷湧來的敵人，撐越久越好。

## 學習重點

### 1. 虛擬搖桿與輸入系統

使用 Joystick Pack 建立觸控搖桿，透過抽象類別 InputBase 設計可切換的輸入系統，同時支援鍵盤與搖桿操作。

### 2. 敵人追蹤 AI

使用 Chaser 腳本讓敵人自動追蹤玩家，設定移動速度與停止距離，搭配 ChaserManager 統一管理所有敵人的目標。

### 3. 武器與傷害系統

透過模組化設計將武器拆分為觸發（WeaponTrigger）與射擊（WeaponShooter）兩個部分，搭配 DamageSender / DamageReceiver 實現通用的傷害機制。

### 4. 敵人生成器

使用 Spawner 在玩家周圍的隨機位置持續生成敵人，可調整生成間隔與生成範圍，讓遊戲難度隨時間遞增。

### 5. 死亡特效與場景重載

為玩家與敵人加入死亡粒子特效（DeadEffect），並透過 ReloadScene 在玩家死亡後自動重新載入場景。

### 6. Android 打包發佈

設定 Android Build Settings、簽署 Keystore，將遊戲打包為 APK 安裝到手機上實際遊玩。

## 開發環境

- Unity 6（URP）
- Adaptive Performance
- Joystick Pack
- TextMeshPro
