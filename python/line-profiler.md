# Line Profiler

To find lines that are slowing down a Python script of function, use the line_profiler module by rkern. 

First install 

```
pip install line_profiler
```

then mark the functions to be profiled with `@profile` before the function definition. Save the python script. Run the following command:

```
kernprof -l python_script.py
```

To view the profiling results, run

```
python -m line_profiler python_script.py.lprof
```


Module Github Source: <https://github.com/rkern/line_profiler>
