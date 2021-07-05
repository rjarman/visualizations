# Visualizations

- Help on function `c_m_visualize` in module `__main__`:

  ```
  c_m_visualize(y_true, y_pred, labels, size, is_num_class=False, extra_r_c_label='precision_recall_accuracy', row_title='Target Class', col_title='Output Class', fig_title='Confusion Matrix', color_bar=False, color_map='YlGn', figsize=(10, 10)) -> <built-in function array>
  src: https://gist.github.com/rjarman/b2a5e00e65ba22554f2d1f4a07fc9532#file-c_m_visualization-py
  y_true: test classes
  y_pred: predicted classes
  labels: list of labels
  size: size of y_true or y_pred
  is_num_class: It indicates that whether a heatmap generates depends on numbers of classes or percentages
  extra_r_c_label: extra column and row label for precision, recall, support and accuracy as a str
  row_title: horizontal title of the figure
  col_title: verticle title of the figure
  fig_title: title of the figure
  color_bar: False means there will be no color bar attached to the figure and vice versa
  color_map: supported color map for sns.heatmap
  figsize: size of the figure

  return: confusion matrix as numpy.ndarray
  ```

  - Examle:
    ```python
    labels = ['Potato__Early_blight', 'Potato__Late_blight',  'Potato__healthy', 'Tomato__Early_blight',  'Tomato__Late_blight', 'Tomato__healthy']
    c_m_visualize(y_true, y_pred, labels, len(y_true))
    c_m_visualize(y_true, y_pred, labels, len(y_true),  is_num_class=True)
    ```

> References

- [How to make a custom confusion matrix on matplotlib with heatmap and annotation](https://blog.heaplinker.com/How-to-make-a-custom-confusion-matrix-on-matplotlib-with-heatmap-and-annotation-2021070218326405004/)
