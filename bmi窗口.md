

```python
import tkinter as tk

root = tk.Tk()

root.title(‘计算BMI值’)

tk.Label(root, text=“体重(单位:kg)：”).grid(row=0, column=0)
tk.Label(root, text=“身高(单位:m)：”).grid(row=1, column=0)

entry1 = tk.Entry(root)
entry2 = tk.Entry(root)
entry1.grid(row=0, column=1, padx=10, pady=10)
entry2.grid(row=1, column=1, padx=10, pady=10)

var_BMI = tk.StringVar()
var_BMI_text = tk.StringVar()

def count():
weight = float(entry1.get())
height = float(entry2.get())
temp_BMI = weight/(height**2)
var_BMI.set(str(temp_BMI))

if temp_BMI<18.5:
var_BMI_text.set(‘体重过轻。’)
elif temp_BMI>=18.5 and temp_BMI<=24.9:
var_BMI_text.set(‘体重正常’)
elif temp_BMI>24.9 and temp_BMI<=30:
var_BMI_text.set(‘体重超重’)
elif temp_BMI>=30:
var_BMI_text.set(‘体重过重了’)

tk.Label(root, text=“BMI值为：”).grid(row=2, column=0)
tk.Label(root, textvariable=var_BMI).grid(row=2, column=1)

tk.Button(root, text=“计算BMI”, width=10, command=count)
.grid(row=10, column=0, sticky=tk.W, padx=20, pady=10)

tk.mainloop()
```


```python


```
