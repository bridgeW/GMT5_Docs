P选项
=====

:mtime: 2015-02-07
:ctime: 2015-05-09

在\ :doc:`paper`\ 一节中说过， 画布有两种放置方式：Portrait模式和Landscape模式。

.. figure:: /images/GMT_-P.*
   :width: 500px
   :align: center
   :alt: paper orientation

由于历史原因，GMT默认使用Landscape模式，可以通过P选项设定使用Portrait模式。

将一个Landscape模式的PS文件与一个Portait模式的PS文件对比可以发现，Landscape模式的PS文件中多了如下代码::

    595 0 T 90 R

这句代码的意思应该是将坐标系移动（\ **T**\ ransition）到(595,0)再旋转（\ **R**\ otate）90度，即由Portrait模式变成Landscape模式。

需要格式注意的是，P选项设置的是\ **画布的属性**\ ，因而对于由多个命令绘制而成的图片来说，只有第一个命令是需要使用P选项的，其他绘图命令中使用或不使用P选项，对最终结果不会有任何影响。
