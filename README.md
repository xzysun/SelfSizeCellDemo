SelfSizeCellDemo
================

一个演示Demo，利用iOS8的新特性来实现UITableViewCell的高度根据内容自动控制

通过设置
<code>
self.tableView.estimatedRowHeight = 68.0;
self.tableView.rowHeight = UITableViewAutomaticDimension;
</code>
配合AutoLayout来实现该功能。

需要注意在InterfaceBuilder中设置Label控件的Content Hugging Pirority和Content Compression Resistance Priority来保证自动调整高度。

P.S. 两个字段的说明
Hugging priority 确定view有多大的优先级阻止自己变大。
Compression Resistance priority确定有多大的优先级阻止自己变小。
