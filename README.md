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


# Date 17th March 2025
## Running third trio

## Pipeline Version
(wdl_test) hassan@node24:/data/humangen_kircherlab/hassan/HiFi-human-WGS-WDL$ git describe --tags
v2.0.7


## Config
Yu3punga$j7dYu3punga$j7d{
  "humanwgs_family.family": {
    "family_id": "ThirdTrio",
    "samples": [
      {
        "sample_id": "S009_X47-24_WGS-Rv-0155",
        "hifi_reads": ["/data/humangen_kircherlab/hassan/bioscientia/r84149R1_20241107_141501/S009_X47-24_WGS-Rv-0155.hifi_reads.bam"],
        "affected": true,
        "father_id": "S011_X49-24_WGS-Rv-0155",
        "mother_id": "S010_X48-24_WGS-Rv-0155"
      },
      {
        "sample_id": "S010_X48-24_WGS-Rv-0155",
        "hifi_reads": ["/data/humangen_kircherlab/hassan/bioscientia/r84149R1_20241107_141501/S010_X48-24_WGS-Rv-0155.hifi_reads.bam"],
        "affected": false,
        "sex": "FEMALE"
      },
      {
        "sample_id": "S011_X49-24_WGS-Rv-0155",
        "hifi_reads": ["/data/humangen_kircherlab/hassan/bioscientia/r84149R1_20241107_141501/S011_X49-24_WGS-Rv-0155.hifi_reads.bam"],
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

## Curr Dir
(wdl_test) hassan@node24:/data/humangen_kircherlab/hassan/HiFi-human-WGS-WDL$ pwd
/data/humangen_kircherlab/hassan/HiFi-human-WGS-WDL

## Command to Run
hassan@headnode01:/data/humangen_kircherlab/hassan/HiFi-human-WGS-WDL$ srun --partition=longterm --mem=256G -c 42 miniwdl run workflows/family.wdl -i backends/hpc/family.hpc.inputs.json --verbose


# Date 18th March 2025
Ran with the above config and the following .sh script
#!/bin/bash

# Capture the current date and time
current_date=$(date +"%Y-%m-%d_%H-%M-%S")
echo "Date and Time is: $current_date"

## Variables
partition="longterm"
nodes=1
cpus=42
memory=256GB 
job_name="FamilyWDL"

### Submit this Script with: sbatch <script.sh> ### 

# Parameters for slurm (don't remove the # in front of #SBATCH!)
#SBATCH --partition=$partition
#SBATCH --nodes=$nodes
#SBATCH -c $cpus
#SBATCH --mem=$memory
#SBATCH --job-name=$job_name

# Set SLURM output file directly
#SBATCH --output=${output_file}

# Print SLURM configuration to output file

echo ""
echo "Requested Resoursces:"

echo "#SBATCH --partition=$partition"
echo "#SBATCH --nodes=$nodes" 
echo "#SBATCH -c $cpus"  
echo "SBATCH --mem=$memory"
echo "SBATCH --job-name=$job_name"


# For conda error
export PATH=/work/hassan/hassan/miniforge/bin:$PATH
source /work/hassan/hassan/miniforge/etc/profile.d/conda.sh

echo ""
# Load your necessary modules:
echo 'Activating the Conda Environment'
conda activate wdl_test
echo "Conda Environment ($CONDA_DEFAULT_ENV) Activated"


# Load Singularity
module load singularity

# Get to the correct Directory
echo ""
echo 'Changing Directory to the WDL Directory'
cd /data/humangen_kircherlab/hassan/HiFi-human-WGS-WDL
echo "Directory Changed to the WDL Directory: $PWD"

# Submit the Command:
echo "Running the following Command"
echo "miniwdl run workflows/family.wdl -i backends/hpc/family.hpc.inputs.json --verbose"
echo ""
echo ""
echo "###################################################"
echo "Pipline Output"
echo "###################################################"



miniwdl run workflows/family.wdl -i backends/hpc/family.hpc.inputs.json --verbose





# Date: 
## Running third trio
## Pipeline Version
## Config
## Curr Dir
## Curr Resources
## Command to run


