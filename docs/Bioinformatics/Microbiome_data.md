
Please see this well put together class https://gibbons-lab.github.io/isb_course_2021/16S/  Links to an external site.- the class materials are also available in a github https://github.com/Gibbons-Lab/isb_course_2021.

To run qiime2 on the HPCC - where it is already installed - you can do this __INSTEAD OF THE EXAMPLE IN THE SITE__

```
source activate qiime2
module load qiime2
```

Remember if you want to do the work in the tutorial you need to setup a job run with an interactive session. This example starts a 2hr job on the short queue - you can replace `-p short` with `-p batch` if you want more time

```
$ srun -p short -N 1 -n 1 -c 8 --mem 24gb --pty bash -l
$ module load qiime2
```
