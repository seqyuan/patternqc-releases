# patternqc

## Install

```bash
# x86_64
curl -LO https://github.com/seqyuan/patternqc-releases/releases/latest/download/patternqc-linux-amd64
chmod +x patternqc-linux-amd64

# ARM64
curl -LO https://github.com/seqyuan/patternqc-releases/releases/latest/download/patternqc-linux-arm64
chmod +x patternqc-linux-arm64
```

## Usage

```bash
./patternqc-linux-amd64 version

# 过滤并输出（可合并多文库）
./patternqc-linux-amd64 filter -r1 lib_R1.fq.gz -r2 lib_R2.fq.gz -outprefix ./out

# 只统计 R2 并给出过滤/加测建议
./patternqc-linux-amd64 qc -r2 lib_R2.fq.gz -outprefix ./out -target-reads 4000000000 -target-map-rate 85
```

`filter -h` / `qc -h` 查看全部参数。
