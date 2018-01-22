# css
利用css的transform创建一个扇形导航
first step
1.用一个无序列表来，将整个圆平均分成8块，每一块的圆心角为x=360deg/8=45deg;
  设置每一项的旋转基点为right bottom;
  我们将这些条目转换到足够的左边，以便它们的转换来源与容器的中心重合。
  旋转每一项，按i*xdeg来旋转，i为无序列表项数，i为中心角度数
2.变形每一项无序列表的值90deg-x;
要创建一个与我们所期望的中心角度值相等的值，我们将不得不通过以下方法对项进行倾斜(使用斜交()CSS函数):
倾斜角度值=90deg-x;x=45deg为中心角度值；
3.倾斜列表项也会导致它们的内容倾斜，从而导致它们的内容被扭曲。这里将要应用以下数学规则(phew!)将确保内容不会被扭曲，并且它们的内容是可见的。
unskew：-x，也即skew：-45deg
不倾斜锚内容，这意味着用来倾斜列表项的相反的值对它们进行倾斜，然后内容按一个值旋转:
- [90 – (x/2) ]=-【90-22.5】=-67.5deg//这里为每项无序列表里的span的rotate值
