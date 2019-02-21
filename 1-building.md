# 1. Building the machine

A machine's specification results from an interplay of budget constraints and user needs. 
In this guide, money is a strong constraint. If this is not the case, then hiring a consulting company is a much better option.

First, decide what the users need. Get to know their past, present, and future workloads.
Understand their tasks: does Alice need a lot of disk space for her databases work? 
Is Bob a GPU hog for his neural machine translation project?
Is Carol a light GPU user who only needs it once in a blue moon?
If the needs are unknown, ask.

Then, choose the parts and the budget. This may restrict what can be provided to the users -- be ready to displease everyone equally. 
If you don't know all the parts of a computer, Google it.
If you don't know how to assemble a computer, Google it.
Here are a few specific tips:

- **Intel CPUs are king.** Desktop AMD CPUs might have more PCIe lanes, but [Intel's Math Kernel Library](https://software.intel.com/en-us/mkl)
far [outshines any slight drawback](https://software.intel.com/en-us/articles/performance-comparison-of-openblas-and-intel-math-kernel-library-in-r) to using an Intel CPU.
- **Using two to three cards is a good form factor.** 
As far as I'm aware, the most number of lanes a desktop Intel CPU offers is 44 -- choose a [PLX](https://linustechtips.com/main/topic/547470-plx-chip-whas-exactly-does-it-do/) motherboard to accomodate three cards better.
- **Invest in a non-stock CPU fan.** [This one](http://www.coolermaster.com/cooling/cpu-air-cooler/hyper-212-evo/) is sufficient for everything I've done.
- **Invest in a big case.** Have two cards? Go for full. Have three cards? Go for XL. 
This allows you to install more fans and improve airflow.
- **Read the GPU benchmarks.** Lambda Labs has a [good one](https://lambdalabs.com/blog/best-gpu-tensorflow-2080-ti-vs-v100-vs-titan-v-vs-1080-ti-benchmark/).
- **Keep all receipts and original packaging.** I tend to throw things out, and this has saved me trouble before.

Finally, stress test the GPUs for 12 hours. [GPU burn](https://github.com/wilicc/gpu-burn) is an excellent utility.
