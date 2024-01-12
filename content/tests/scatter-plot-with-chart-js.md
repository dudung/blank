+++
title = 'Scatter plot with Chart.js'
date = 2024-01-12T08:18:18+07:00
draft = false
+++
Create shortcode for scatter plot with [Chart.js](https://www.chartjs.org/).


## create post
```
$ hugo new content tests/scatter-plot-with-chart-js.md
Content "D:\\blank\\content\\tests\\scatter-plot-with-chart-js.md" created
```

It is placed in `content/tests` folder while the shortcode being developed.



## tests
{{< blank/scatter  >}}
5.000,3.000
4.618,4.176
3.618,4.902
2.382,4.902
1.382,4.176
1.000,3.000
1.382,1.824
2.382,1.098
3.618,1.098
4.618,1.824

11.000,3.000
10.853,3.927
10.427,4.763
9.763,5.427
8.927,5.853
8.000,6.000
7.073,5.853
6.237,5.427
5.573,4.763
5.147,3.927
5.000,3.000
5.147,2.073
5.573,1.237
6.237,0.573
7.073,0.147
8.000,0.000
8.927,0.147
9.763,0.573
10.427,1.237
10.853,2.073
{{< /blank/scatter >}}






## generate data
```
import math

def circlePoints(xc, yc, R, N):
  M = round(360 / N);

  xx = []
  yy = []
  for i in range(N):
    q = i * (math.pi / 180) * M
    x = xc + R * math.cos(q)
    y = yc + R * math.sin(q)
    xx.append(x)
    yy.append(y)    
  
  return [xx, yy]

N1 = 10
[x1, y1] = circlePoints(3, 3, 2, N1)
for i in range(min(len(x1), len(y1))):
  print(
    f'{x1[i]:.3f}', 
    f'{y1[i]:.3f}',
    sep=','
  )

print()

N2 = 20
[x2, y2] = circlePoints(8, 3, 3, N2)
for i in range(min(len(x2), len(y2))):
  print(
    f'{x2[i]:.3f}', 
    f'{y2[i]:.3f}',
    sep=','
  )
```
url https://onecompiler.com/python/3zz6tddvh
