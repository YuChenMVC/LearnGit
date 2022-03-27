# Conventional Commits

<br>

## Standard
```
<type>: [subject]

[description]

[issue number]
```

<br>

## Illustrations

`type 種類`
> feat 新增擴充
\
> fix 修補
\
> docs 文件
\
> style 格式
\
> refactor 重構
\
> perf 效能最佳化
\
> test 測試功能
\
> build 建置系統
\
> ci 自動化CI/CD
\
> revert 回復commit

`subject` 
> 總結你做了什麼

`description` 
> 詳述為什麼修改及變動修改的原因

`issue` 
> 如果有 填寫issue編號

\
~~不一定要照我的 跟RESTful一樣是種規範~~

<br>

## Example of use

```
feat: UploadFileController上傳檔案功能

客戶需求:
1.客戶直接打來要求一堆 需求常改來改去
2.PM反應客戶要求上傳速度快一點 不然每次批次檔都要等很久

調整項目:
1.應應快速需求對Controller與Service解耦合
2.Controller邏輯IFormFile改用Collection<T>解一次讀取多個檔案

issue #200
```

<br>

## Resources
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)\
[Contributing to Angular](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#type)

