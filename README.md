SelfSizeCellDemo
================

一个演示Demo，利用iOS8的新特性来实现UITableViewCell的高度根据内容自动控制

通过设置
<br/>
<code>
self.tableView.estimatedRowHeight = 68.0;
</code>
<br/>
<code>
self.tableView.rowHeight = UITableViewAutomaticDimension;
</code>
<br/>
配合AutoLayout来实现该功能。

需要注意在InterfaceBuilder中设置Label控件的Content Hugging Pirority和Content Compression Resistance Priority来保证自动调整高度。
<br/>
在Demo中，Cell拥有NameLabel和AddressLabel两个文本控件。两个控件的高度都未pin到固定值，NameLabel的Vertical Hugging Priority为251，比默认的250大，所以它的高度固定不变。AddressLabel的Vertic Hugging Priority为249，比默认的250小，所以它的高度是可以根据内容自动增长的。同时两个控件的Vertical Compression Resistance Priority都是默认的750，在高度压缩上采用默认的行为。

P.S. 两个字段的说明:<br/>
Hugging priority 确定view有多大的优先级阻止自己变大。<br/>
Compression Resistance priority确定有多大的优先级阻止自己变小。
