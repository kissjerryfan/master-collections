### 'numpy.float64' object does not support item assignment
这个问题在我进行numpy数组的赋值时遇到，代码片段如下
```python
fc_vec = np.zeros((n*n, 1)).squeeze()
fc_vec[row[i]][col[i]] = cb_val[i]
```
这段代码的主要目的是为了将fc_vec的某个位置的元素替换成cb_val中对应位置的元素，但是就出现了上面的报错，在查了很多文章之后，出现的原因基本都是使用了同名数组。直到找到了一个人遇到的类似问题，给了我一些启发

主要原因是fc_vec是一个np.zeros方法直接生成的scalar类，这样的类型不支持像普通的数组一样进行直接按索引取值，而是要使用切片的方式，因此要将赋值语句改为
```
fc_vec[row[i], col[i]] = cb_val[i]
```

### setting an array element with a sequence
