
Regarding the workload factor just consider a higher setting for CPU-bound workloads, so the more insense use of CPU the more workload factor.

This workload sometimes is difficult to predict in the projects as each project is a different battle and nothing is 100% 'able to be predicted'

Regarding the size just common sense and having help from https://www.cloudera.com/documentation/enterprise/5-3-x/topics/cdh_ig_yarn_tuning.html

So + 16 Gb of RAM just in case if the RAM that we allocate in the spreadsheet is not enough and + 3c because a service can override the 
maximum number of cores that we assign. Basically the system must have enought cores and RAM to perform well.

This is a prediction. It's important to monitor how it runs in the later stages of a project or when production stack is going to be released.

Some heap was increased as well. Just in case.
