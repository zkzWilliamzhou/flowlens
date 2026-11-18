# FlowLens - Shell 工作流程透镜

## 项目名称
**FlowLens**

## GitHub Repository Description
Analyze shell workflow patterns and generate optimized command sequences. Discover your command DNA, find inefficiencies, and automate repetitive tasks. Pure shell with zero dependencies.

## 项目描述
FlowLens 分析你的 shell 工作流程，提供优化建议，生成自动化脚本，将重复工作变为一次可复用。

### 核心痛点

1. **重复劳动**：同样的命令序列反复执行
2. **效率瓶颈**：不知道如何优化工作流程
3. **知识孤岛**：个人经验无法沉淀
4. **自动化盲区**：不知道从哪开始自动化

## 核心功能

### 1. 工作流程分析 🔍
- 命令序列识别
- 重复模式检测
- 效率评分

### 2. 优化建议 💡
- 生成优化脚本
- 建议别名
- 建议函数

### 3. 自动化生成 🤖
- 从模式生成脚本
- 交互式优化
- 一键应用

## 使用示例

```python
from flowlens import FlowLens

lens = FlowLens(history_file="~/.bash_history")

patterns = lens.find_patterns(min_occurrence=5)
print(f"发现 {len(patterns)} 个重复模式")

for pattern in patterns:
    print(f"模式: {pattern.commands}")
    print(f"出现次数: {pattern.count}")
    print(f"建议: {pattern.suggestion}")
    
    # 生成优化脚本
    script = lens.generate_script(pattern)
    script.save("optimized.sh")
```

## License
MIT License