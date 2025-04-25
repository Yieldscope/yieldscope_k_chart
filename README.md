This is a fork on this <href>https://github.com/OpenFlutter/k_chart</href> library.

In this fork, we have made the following changes (keep updates):
1. Expose chart `scrollX`, `scaleX`, `selectX` and `selectY` to `onScroll` and `onLoadMore` callback. Accept `scaleLevel` and `scrollPosition` in `KChartWidget` constructor.
   Reason doing such changes: Usually we use `onLoadMore` to fetch more data to the Widget's datas, but when datas changes, it will trigger rebuild of the chart and reset the scroll position and zoom level to the default one. So if you change the state when onLoadMore, just pass the `scrollX` and `scaleX` to the `scaleLevel` and `scrollPosition` to preserve the original chart states.
