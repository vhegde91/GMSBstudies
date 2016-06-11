./splitLooper.sh GJets_HT-400To600 signalRegionSkim <br \>

./splitLooper.sh : Submit one job per file for the dataset GJets_HT-400To600. signalRegionSkim is the name of the executable in ../src/
spawnJobs.py : Creates and(or) submits condor job. Creates one .jdl file. This is called by ./splitLooper.sh many times with a few arguments.
my_looper.sh : Contains commands for submitting jobs on different datasets.
findFailedJobs.C : Runs inside root. It compares .jdl files and the output root files and tells you which are failed jobs. You can copy the output of this to submitFailedJobs.sh and do ./submitFailedJobs.sh to resubmit the failed jobs.
cleanUpBatch.sh : Clears .jdl,.stderr, .stdout, .condor files
