#代码行数统计

- 统计当前文件夹下所有代码：  
`find . -name "*.[hm]" -print0 | xargs -0 wc -l`   
- 排除当前文件夹下名为 3rdLib 的目录   
`find . -path "./3rdLib" -prune -o  -name "*.[hm]" -print0 | xargs -0 wc -l`

