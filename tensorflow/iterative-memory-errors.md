# Iterative Loops Memory Errors

When creating graphs within iterative loops, 
`tf.reset_default_graph()` needs to be used 
to avoid variable initialization errors. This
can eventually lead to memory errors after a 
few iterations, either from the GPU directly
or the RAM. Related online threads:

* (https://github.com/tensorflow/tensorflow/issues/1727)
* (http://stackoverflow.com/questions/36521908/how-to-iteratively-create-tensorflow-graphs-on-the-fly-without-accumulating-memo)
