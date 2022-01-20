const link = document.createElement('a') // 创建元素
# const blob = new Blob([res], { type: 'application/vnd.ms-excel' })
link.style.display = 'none'
link.href = URL.createObjectURL(blob) // 创建下载的链接
link.setAttribute('download', flag == 1 ? '时间明细统计表' : '总统计表' +'.xlsx') // 给下载后的文件命名
document.body.appendChild(link)
link.click() // 点击下载
document.body.removeChild(link) //  下载完成移除元素
window.URL.revokeObjectURL(link.href) // 释放掉blob对象
