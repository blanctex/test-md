# 🪟 Windows Tips: 最近使った項目（shell:recent）をクイックアクセスに追加

## ✨ 問題意識

Windows 7 では設定により、スタートメニューから「最近使ったファイル」を表示することが可能だった。  
これは Windows 10 / 11 の「最近使ったファイル」機能とは異なり、**純粋に開いたファイル**を時系列で並べることができた。

しかし、Windows 10 の「クイックアクセス」、Windows 11 の「ホーム - クイックアクセス」は、  
**何をもって“最近”とするかが曖昧で、目的のファイルが出てこない**ことがある。

---

## 🔎 対策

`shell:recent` をクイックアクセスに登録することで、  
**OSが記録している本当の“最近使ったファイル・フォルダ”**を一覧表示できる。

---

## 🛠 手順

### 1. Windows 10 / 11 の表示の違いに注意

- **Windows 10**：エクスプローラー → ホーム → クイックアクセス
- **Windows 11（22H2以降）**：クイックアクセスは「ホーム」に統合

### 2. フォルダオプション（オプション設定）

エクスプローラー上部の「表示」→「オプション」→「フォルダーオプション」を開く

- プライバシー設定のチェックボックスを確認：
  - ☑ 最近使用したファイルを表示する
  - ☑ 頻繁に使用されるフォルダーを表示する
  - ☑ Office.com のファイルを表示する（必要に応じて）

### 3. `shell:recent` をクイックアクセスに登録

1. エクスプローラーのアドレスバーに `shell:recent` と入力してEnter
2. 開かれたフォルダ上で右クリック → 「上のフォルダへ移動」
3. `Recent` フォルダを右クリック → 「クイックアクセスにピン留め」

※ 最大 150 件程度の `.lnk`（ショートカット）が記録されている。

---

## 💡 効果

- ファイル・フォルダ問わず時系列で**約149件程度**表示される
- 記録は自動的に更新され、**直近の作業がそのまま反映される**
- **記憶を手がかりにファイルを探す**という用途に極めて有効

---

## 📝 補足

- `.lnk`形式で記録されるため、**本体は含まれない**
- Officeやブラウザ系アプリでは、履歴が残らないこともある
- ファイルのみ or フォルダのみ抽出するには `shell:recent\*` の絞り込みが有効

---

## 📚 関連情報

- Windows Script Programmer 2019 による関連Tips：  
  https://answers.microsoft.com/ja-jp/windows/forum/all/%E3%82%AF%E3%82%A4%E3%83%83%E3%82%AF/61f70cde-50a9-401d-8129-43c75ae06394
- Windows 11のエクスプローラーを使いこなそう（Windows10 とWindows11の違い）：  
　https://azby.fmworld.net/usage/closeup/20240131/
