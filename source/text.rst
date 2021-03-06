.. index:: ! fonts

文字
====

:ctime: 2014-11-14
:mtime: 2015-04-17

前面几节说了GMT中如何画线条以及如何填充颜色，这节说说文字的那些事。

文字，或者称文本或字符串，主要由三个属性控制，\ *size*\ ，\ *fonttype*\ 和\ *fill*\ ，三个选项之间用逗号分隔，即\ ``size,fonttype,fill``\ 。三者均是可选的，若其中任意一个属性被省略，则使用该属性的默认值或上一次的设置值。

size
----

字号，即文本大小，通常单位默认是p，但也可加上c、p或者i显式指定单位，比如\ ``15``\ 或\ ``15p``\ 。

fonttype
--------

字体名（区分大小写）或字体对应的ID，比如\ ``Helvetica-Bold``\ 或\ ``1``\ 。

大多数PostScript解释器都内置35种标准字体，至少ghostscript如此，由于GMT以PostScript作为输出，故而GMT默认支持且只支持35种字体。若你使用的PS解释器不支持其中某些字体，则会自动用默认字体（一般是Courier）替换需要的字体。

下图给出了GMT支持的35种字体的列表：

.. figure:: /images/GMT_fonts.*
   :width: 600 px
   :align: center

   GMT可使用的35种PS标准字体

其中，大多数字体都很直观，比较特别的字体有两个，Symbol（12号）和ZapfDingbats（34号），稍后再说。

fill
----

可以为文本填充颜色或图案，参见\ :doc:`fill`\ 一节。

除此之外，文本填充还有更多的特性：

- 在\ *fill*\ 后加上\ **=**\ *pen*\ 来指定如何绘制文本的轮廓，其中\ *pen*\ 参见\ :doc:`pen`\ 一节；
- 设置\ *fill*\ 为\ ``-``\ ，则不对文本进行填充，即空心文字；

示例
----

下图给出了几种指定文本属性的方式

.. figure:: /images/GMT_text.*
   :width: 600 px
   :align: center

   GMT文本属性示例
