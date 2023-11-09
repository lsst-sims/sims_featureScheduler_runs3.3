Check to see if we get identical results after splitting off rubin_sim



Flushed 43907 observations from queue for being stale
Completed 460848 observations
ran in 47 min = 0.8 hours
Writing results to  baseline_sim_v3.3_2yrs.db

Flushed 45529 observations from queue for being stale
Completed 460668 observations
ran in 91 min = 1.5 hours
Writing results to  baseline_sched_v3.3_2yrs.db

--------------

So, unfortunatly the new code is slower and does not give identical results. Booooo.
These are ever so slightly different versions of python. So, let's try doing a clean install of each and running

python baseline_sched.py --survey_length 730 --verbose

Looks like this is taking 3.11 GB 

numpy                     1.26.0          py312h696b312_0    conda-forge
------


Bet this is from replacing palpy with astropy in some places. I bet this is the LSMT calculation.
----



second run:
progress = 99.99%Skipped 0 observations
Flushed 43907 observations from queue for being stale
Completed 460848 observations
ran in 51 min = 0.9 hours
Writing results to  baseline_sim_v3.3_2yrs.db


----

Running with fast LST calc. This seems to work fine.

Flushed 44922 observations from queue for being stale
Completed 460579 observations
ran in 48 min = 0.8 hours
Writing results to  baseline_sched_v3.3_2yrs.db