# MMTQ

MMTQ efficiently mines for all possible patterns in a given trace file within a given time bound and stores in a dictionary as a CSV file. Further postprocessing on the produced dictionary can be performed for a quantitative summary.

### How do I get set up? ###

Execute the following to install necessary dependencies:
```
  $ sudo apt install libboost-all-dev
```
Read [this](#How-to-run-tests) for execution.

### Configuration

Using the make file, one can change configurations for the mining software. Following are the flags that can be used for configuration :
* THREADS : *Count of thread :*
* CSVOUTPUT : *Flag for enabling/disabling CSV output. Takes 0/1*
* DISPLAY_MAP : *Flag for enabling/disabling dumping mined pattern output in stdout*
* TRACE_EM_PATH : *Input file path for Event trace*
* TRACE_TIME_PATH : *Input file path for time associated with each event/quantifier*
* OUTPUT_FILE_PATH : *Output file path for CSV dump. Will be used only if CSVOUTPUT is enabled*
* DO_AGGREGATE : *Flag to signal aggregation of all mined pattern. Takes 0/1*
* OUTPUT_FILE_PATH_AGG : *Output file path for aggregated CSV dump. Will be used only if DO_AGGREGATE is enabled*

### Dependencies
* [GCC 9.3+](https://gcc.gnu.org/)
* [OpenMP 5.0](https://www.openmp.org/)

### How to run tests
Basic commands can be broken into two parts: generating synthetic testcase and mining for valid match.

##### Test Case Generation
Generates the necessary synthetic test case (QRET-timed).
```
make tracegen
```
This command will generate 2 files : 
* Event and/or Quantifiable integer
* Timing for each event and/or quantifiable integer

##### Data Mining with timed constraint
Upon execution, the user must enter their time bounded regex pattern (QRE-timed) along with the alphabet size.
```
make main
```
### Result
#### Android Application usage analysis

**Battery usage between 2 android application**
![2app usage](images/Android%20application%202%20app.png)

**Battery usage between 3 android application**
![3app usage](images/Android%20application%203%20app.png)

**Monitoring battery usage**
![battery usage](images/Battery%20usage%20monitoring.png)

#### Webserver request analysis
**Webserver request analysis**
![webserver request usage](images/Webserver%20request%20analysis.png)

**Webserver request monitoring**
![webserver request monitor](images/Webserver%20request%20monitoring.png)

#### Diabetes Patient analysis
![diabetes analysis](images/diabetes%20analysis.png)

#### Earthquake reading analysis
![earthquake analysis](images/earthquake%20sensor%20analysis.png)

## License
Restricted License. Cannot be replicated or used without prior authorization.
