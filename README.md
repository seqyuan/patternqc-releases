# PatternQC — 10X 3' 文库 TSO 模糊识别、统计与过滤

[![Release](https://img.shields.io/github/v/release/seqyuan/patternqc-releases)](https://github.com/seqyuan/patternqc-releases/releases)

Binary releases for PatternQC. Download, run.

## Quick Install

```bash
# x86_64
curl -LO https://github.com/seqyuan/patternqc-releases/releases/latest/download/patternqc-linux-amd64
chmod +x patternqc-linux-amd64

# ARM64
curl -LO https://github.com/seqyuan/patternqc-releases/releases/latest/download/patternqc-linux-arm64
chmod +x patternqc-linux-arm64
```

## Verify

```bash
sha256sum -c SHA256SUMS
```

## Usage

```bash
./patternqc version

# 过滤并输出（可合并多文库）
./patternqc filter -r1 lib_R1.fq.gz -r2 lib_R2.fq.gz -outprefix ./out

# 只统计 R2 并给出过滤/加测建议
./patternqc qc -r2 lib_R2.fq.gz -outprefix ./out -target-reads 4000000000 -target-map-rate 85
```

## Source Code

本仓库**仅包含发布二进制**，不含源码。源码为私有仓库，授权请联系作者。

## Support

请提交 [Issue](https://github.com/seqyuan/patternqc-releases/issues) 或联系作者。
