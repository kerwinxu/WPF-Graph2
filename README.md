# WPF-Graph
WPF .NET framework Graph control

我增加了注释，关于这个控件，我这里做一下总结。  
关于界面部分：
   1. 依赖属性“CurvesSource="{Binding Curves}"”是曲线的数据。
   2. 内部“<local:ChartControl.Template>”表明这个可以自定义界面。
   3. 画布得是“Canvas x:Name="PART_CHART"”
   4. 同理x轴是 PART_XAXIS，y轴是PART_YAXIS

关于数据部分，这个可以绘制多种曲线，比如：  
   1. new AreaCurve(fs, vs_up, fs, vs, ChartType.Area) 是区域（两条线围起来），
   2. new Curve(f, v, ChartType.Line) 是曲线
   3. new Curve(fs, vs, ChartType.Bar) 是条状的

这些曲线都保存在 “public ObservableCollection<Curve> Curves { get; set; }”中。

界面更新 : Curve.RequestUpdate 方法会更新。

![chart](https://user-images.githubusercontent.com/89906/129889984-1eb52333-e547-44a6-9087-7e20afd8805d.png)
