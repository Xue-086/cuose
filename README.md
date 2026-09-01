# 2026 秋季泛函分析课程主页

这是为 `xue-086/cuose` 整理的课程主页框架。

## 你平时只需要碰两个地方

- `_data/`：改文字、日期、课程安排、作业信息
- `files/`：上传 PDF

HTML、CSS、JavaScript 平时不要动。

## 唯一的文件路径规则

```text
files/
├── lecture-notes/   # 老师课件 / 讲义
├── homework/        # 作业题目
├── solutions/       # 作业答案
└── tutorials/       # 习题课材料
```

这四个目录里的 `README.txt` 可以一直留着，它们只是为了让 GitHub 能显示空文件夹。

## 发布一份课程课件

假设文件名为 `lecture01.pdf`：

1. 上传到 `files/lecture-notes/lecture01.pdf`
2. 打开 `_data/schedule.yml`
3. 在对应周填写：

```yaml
lecture_file: "lecture01.pdf"
```

只写文件名，不要写完整路径。

## 发布作业

把 `hw01.pdf` 上传到 `files/homework/`，然后在 `_data/homework.yml` 加：

```yaml
- id: 1
  title_zh: "作业 1"
  title_en: "Homework 1"
  file: "hw01.pdf"
  solution: ""
  note_zh: ""
  note_en: ""
```

如果课程安排表也要出现“作业 1”按钮，在 `_data/schedule.yml` 对应周填写：

```yaml
homework_id: 1
```

## 发布答案

把 `hw01-solution.pdf` 上传到 `files/solutions/`，然后：

```yaml
solution: "hw01-solution.pdf"
```

## 发布习题课

把 PDF 上传到 `files/tutorials/`，然后在 `_data/tutorials.yml` 加：

```yaml
- date: "2026-09-11"
  title_zh: "习题课 1"
  title_en: "Tutorial 1"
  file: "tutorial01.pdf"
```

## 网站路径

这个版本已经固定为：

```yaml
baseurl: "/cuose"
url: "https://xue-086.github.io"
```

对应网站：

`https://xue-086.github.io/cuose/`

不要再改成 `/course/26FallFA`。
