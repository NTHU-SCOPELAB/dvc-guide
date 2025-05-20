# 如何在Cluster上使用DVC (Data Version Control) (WIP)

- 提高資料集在cluster有限的空間裡的利用率，同時也讓你的實驗除了程式之外也能版控你的訓練資料。
- 因此，DVC是你凖時畢業的好伙伴。

## 1. 安裝dvc
```bash
pip install dvc
```

## 2. 使用dvc初始化你的repository(需已為git repository)
```bash
dvc init
```

## 3. 將dvc的快取指向共用的資料夾
```bash
dvc cache dir /home/shared/dvc-cache
dvc config cache.shared group
dvc config cache.type symlink
```

## 4.a 使用dvc抓取你的資料(如果還沒抓資料)
- https://dvc.org/doc/command-reference/get
- https://dvc.org/doc/command-reference/get-url
- https://dvc.org/doc/command-reference/import
- https://dvc.org/doc/command-reference/import-url
- https://dvc.org/doc/user-guide/integrations/huggingface

## 4.b 將已抓下來的資料加入dvc的追蹤
```bash
dvc add 你的資料集
```
