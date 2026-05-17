# 查看当前状态
git log --oneline -3

# 把本地多出的那个提交取消掉（保留修改内容）
git reset --soft origin/main

# 查看状态确认
git status
git checkout main
# 1. 创建你的分支
git checkout -b feature/jieyufei-qrcode

# 2. 写入二维码方案
echo "签到方案A（jieyufei）：采用二维码签到，工作人员扫码确认" > docs/conflict.md

# 3. 提交
git add docs/conflict.md
git commit -m "feat(jieyufei): 添加二维码签到方案"

# 4. 切换回 main
git checkout main

# 5. 合并你的分支到 main
git merge feature/jieyufei-qrcode -m "merge: 合并二维码签到方案"
git push origin main
