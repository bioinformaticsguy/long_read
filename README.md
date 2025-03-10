# long_read


Link for benchmarks on GIAB: https://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/data/AshkenazimTrio/analysis/




## 10th March 2025
# Running the 2nd Trio Analysis in WDL

## Config
{
  "humanwgs_family.family": {
    "family_id": "SecondTrio",
    "samples": [
      {
        "sample_id": "S005_X32-24_WGS-Rv-0150",
        "hifi_reads": ["/data/humangen_kircherlab/hassan/bioscientia/r84149R1_20241028_142244/S005_X32-24_WGS-Rv-0150.hifi_reads.bam"],
        "affected": true,
        "sex": "FEMALE",
        "father_id": "S007_X34-24_WGS-Rv-0150",
        "mother_id": "S006_X33-24_WGS-Rv-0150"
      },
      {
        "sample_id": "S006_X33-24_WGS-Rv-0150",
        "hifi_reads": ["/data/humangen_kircherlab/hassan/bioscientia/r84149R1_20241028_142244/S006_X33-24_WGS-Rv-0150.hifi_reads.bam"],
        "affected": false,
        "sex": "FEMALE"
      },
      {
        "sample_id": "S007_X34-24_WGS-Rv-0150",
        "hifi_reads": ["/data/humangen_kircherlab/hassan/bioscientia/r84149R1_20241028_142244/S007_X34-24_WGS-Rv-0150.hifi_reads.bam"],
        "affected": false,
        "sex": "MALE"
      }
    ]
  },
  "humanwgs_family.phenotypes": "String? (optional)",
  "humanwgs_family.ref_map_file": "backends/hpc/GRCh38.ref_map.v2p0p0.hpc.tsv",
  "humanwgs_family.tertiary_map_file": "backends/hpc/GRCh38.tertiary_map.v2p0p0.hpc.tsv",
  "humanwgs_family.backend": "HPC",
  "humanwgs_family.gpu": true,
  "humanwgs_family.preemptible": true
}


## Command to run
miniwdl run workflows/family.wdl -i backends/hpc/family.hpc.inputs.json --verbose
### Curr Dir
/data/humangen_kircherlab/hassan/HiFi-human-WGS-WDL

## Curr Resoursces
(wdl_test) hassan@node24:/data/humangen_kircherlab/hassan/HiFi-human-WGS-WDL$ scontrol show job $SLURM_JOB_ID
JobId=1380987 JobName=bash
   UserId=hassan(1001) GroupId=Public(1000) MCS_label=N/A
   Priority=2458 Nice=0 Account=hassan QOS=normal
   JobState=RUNNING Reason=None Dependency=(null)
   Requeue=1 Restarts=0 BatchFlag=0 Reboot=0 ExitCode=0:0
   RunTime=2-18:32:41 TimeLimit=14-00:00:00 TimeMin=N/A
   SubmitTime=2025-03-07T15:18:20 EligibleTime=2025-03-07T15:18:20
   AccrueTime=Unknown
   StartTime=2025-03-07T15:18:20 EndTime=2025-03-21T15:18:20 Deadline=N/A
   SuspendTime=None SecsPreSuspend=0 LastSchedEval=2025-03-07T15:18:20
   Partition=longterm AllocNode:Sid=headnode01:29891
   ReqNodeList=(null) ExcNodeList=(null)
   NodeList=node24
   BatchHost=node24
   NumNodes=1 NumCPUs=42 NumTasks=1 CPUs/Task=42 ReqB:S:C:T=0:0:*:*
   TRES=cpu=42,mem=256G,node=1,billing=42
   Socks/Node=* NtasksPerN:B:S:C=0:0:*:* CoreSpec=*
   MinCPUsNode=42 MinMemoryNode=256G MinTmpDiskNode=0
   Features=(null) DelayBoot=00:00:00
   OverSubscribe=OK Contiguous=0 Licenses=(null) Network=(null)
   Command=bash
   WorkDir=/data/humangen_kircherlab/hassan/HiFi-human-WGS-WDL
   Power=
   NtasksPerTRES:0

