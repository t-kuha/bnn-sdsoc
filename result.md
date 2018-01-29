### Performance Estimation Result

#### 1. LOOP_TRIPCOUNT

```XML
<?xml version="1.0" encoding="UTF-8"?>
<est:Report xmi:version="2.0" xmlns:xmi="http://www.omg.org/XMI" xmlns:est="http://www.xilinx.com/est">
  <graph hwLatency="1182975721">
    <function name="top" file="AccelSchedule.cpp" line="123"/>
  </graph>
  <resources>
    <resource name="dsp" used="4" total="220"/>
    <resource name="bram" used="62" total="140"/>
    <resource name="lut" used="31647" total="53200"/>
    <resource name="ff" used="26296" total="106400"/>
  </resources>
</est:Report>
```

* Timing (ns): 

|  Clock | Target| Estimated| Uncertainty|
|-------:|------:|---------:|-----------:|
|ap_clk  |  10.00|      7.28|        2.70|


* Latency (clock cycles): 

|     Latency    | |    Interval    | | Pipeline|
|-----:|----------:|-----:|----------:|--------:|
|  min |    max    |  min |    max    |   Type  |
|  4781|  177419856|  4781|  177419856|   none  |


* Utilization Estimates: 

|       Name      | BRAM_18K| DSP48E|   FF   |  LUT  |
|:---------------:|--------:|------:|-------:|------:|
|DSP              |        -|      1|       -|      -|
|Expression       |        -|      -|       0|    877|
|FIFO             |        -|      -|       -|      -|
|Instance         |       10|      3|    3600|  13494|
|Memory           |       50|      -|       0|      0|
|Multiplexer      |        -|      -|       -|    448|
|Register         |        -|      -|     304|      -|
|Total            |       60|      4|    3904|  14819|
|Available        |      280|    220|  106400|  53200|
|Utilization (%)  |       21|      1|       3|     27|


***
### 2. + PIPELINE

```XML
<?xml version="1.0" encoding="UTF-8"?>
<est:Report xmi:version="2.0" xmlns:xmi="http://www.omg.org/XMI" xmlns:est="http://www.xilinx.com/est">
  <graph hwLatency="327462228">
    <function name="top" file="AccelSchedule.cpp" line="123"/>
  </graph>
  <resources>
    <resource name="dsp" used="4" total="220"/>
    <resource name="bram" used="61" total="140"/>
    <resource name="lut" used="62925" total="53200"/>
    <resource name="ff" used="35855" total="106400"/>
  </resources>
</est:Report>
```

+ Timing (ns): 

|  Clock | Target| Estimated| Uncertainty|
|-------:|------:|---------:|-----------:|
|ap_clk  |  10.00|      8.42|        2.70|


+ Latency (clock cycles): 

|     Latency   | |     Interval  | | Pipeline|
|-----:|---------:|-----:|---------:|--------:|
|  min |    max   |  min |    max   |   Type  |
|  4775|  49092836|  4775|  49092836|   none  |


* Utilization Estimates: 

|       Name      | BRAM_18K| DSP48E|   FF   |  LUT  |
|:---------------:|--------:|------:|-------:|------:|
|DSP              |        -|      1|       -|      -|
|Expression       |        -|      -|       0|    973|
|FIFO             |        -|      -|       -|      -|
|Instance         |        8|      3|   13118|  44514|
|Memory           |       50|      -|       0|      0|
|Multiplexer      |        -|      -|       -|    610|
|Register         |        -|      -|     345|      -|
|Total            |       58|      4|   13463|  46097|
|Available        |      280|    220|  106400|  53200|
|Utilization (%)  |       20|      1|      12|     86|


#### 3. + UNROLL

```XML
<?xml version="1.0" encoding="UTF-8"?>
<est:Report xmi:version="2.0" xmlns:xmi="http://www.omg.org/XMI" xmlns:est="http://www.xilinx.com/est">
  <graph hwLatency="327462228">
    <function name="top" file="AccelSchedule.cpp" line="123"/>
  </graph>
  <resources>
    <resource name="dsp" used="4" total="220"/>
    <resource name="bram" used="61" total="140"/>
    <resource name="lut" used="63141" total="53200"/>
    <resource name="ff" used="35752" total="106400"/>
  </resources>
</est:Report>
```


+ Timing (ns): 

|  Clock | Target| Estimated| Uncertainty|
|-------:|------:|---------:|-----------:|
|ap_clk  |  10.00|      8.42|        2.70|


* Utilization Estimates:  

|       Name      | BRAM_18K| DSP48E|   FF   |  LUT  |
|:---------------:|--------:|------:|-------:|------:|
|DSP              |        -|      1|       -|      -|
|Expression       |        -|      -|       0|    973|
|FIFO             |        -|      -|       -|      -|
|Instance         |        8|      3|   13015|  44730|
|Memory           |       50|      -|       0|      0|
|Multiplexer      |        -|      -|       -|    610|
|Register         |        -|      -|     345|      -|
|Total            |       58|      4|   13360|  46313|
|Available        |      280|    220|  106400|  53200|
|Utilization (%)  |       20|      1|      12|     87|


***
#### 4. + INLINE

```XML
<?xml version="1.0" encoding="UTF-8"?>
<est:Report xmi:version="2.0" xmlns:xmi="http://www.omg.org/XMI" xmlns:est="http://www.xilinx.com/est">
  <graph hwLatency="3734858">
    <function name="top" file="AccelSchedule.cpp" line="123"/>
  </graph>
  <resources>
    <resource name="dsp" used="4" total="220"/>
    <resource name="bram" used="80" total="140"/>
    <resource name="lut" used="76964" total="53200"/>
    <resource name="ff" used="37952" total="106400"/>
  </resources>
</est:Report>
```


+ Timing (ns): 

|  Clock | Target| Estimated| Uncertainty|
|-------:|------:|---------:|-----------:|
|ap_clk  |  10.00|      8.42|        2.70|


+ Latency (clock cycles): 

|    Latency  | |    Interval | | Pipeline|
|-----:|-------:|-----:|-------:|--------:|
|  min |   max  |  min |   max  |   Type  |
|  4775|  533732|  4775|  533732|   none  |


* Utilization Estimates: 

|       Name      | BRAM_18K| DSP48E|   FF   |  LUT  |
|:---------------:|--------:|------:|-------:|------:|
|DSP              |        -|      1|       -|      -|
|Expression       |        -|      -|       0|    973|
|FIFO             |        -|      -|       -|      -|
|Instance         |       46|      3|   15215|  58562|
|Memory           |       50|      -|       0|      0|
|Multiplexer      |        -|      -|       -|    601|
|Register         |        -|      -|     345|      -|
|Total            |       96|      4|   15560|  60136|
|Available        |      280|    220|  106400|  53200|
|Utilization (%)  |       34|      1|      14|    113|


***
#### 5. + DEPENDENCE

```XML
<?xml version="1.0" encoding="UTF-8"?>
<est:Report xmi:version="2.0" xmlns:xmi="http://www.omg.org/XMI" xmlns:est="http://www.xilinx.com/est">
  <graph hwLatency="14217192">
    <function name="top" file="AccelSchedule.cpp" line="123"/>
  </graph>
  <resources>
    <resource name="dsp" used="4" total="220"/>
    <resource name="bram" used="81" total="140"/>
    <resource name="lut" used="77673" total="53200"/>
    <resource name="ff" used="36679" total="106400"/>
  </resources>
</est:Report>
```


+ Timing (ns): 

|  Clock | Target| Estimated| Uncertainty|
|-------:|------:|---------:|-----------:|
|ap_clk  |  10.00|      8.42|        2.70|

+ Latency (clock cycles): 

|     Latency  | |    Interval  | | Pipeline|
|-----:|--------:|-----:|--------:|--------:|
|  min |   max   |  min |   max   |   Type  |
|  4775|  2106082|  4775|  2106082|   none  |


* Utilization Estimates: 

|       Name      | BRAM_18K| DSP48E|   FF   |  LUT  |
|:---------------:|--------:|------:|-------:|------:|
|DSP              |        -|      1|       -|      -|
|Expression       |        -|      -|       0|    973|
|FIFO             |        -|      -|       -|      -|
|Instance         |       48|      3|   13942|  59271|
|Memory           |       50|      -|       0|      0|
|Multiplexer      |        -|      -|       -|    601|
|Register         |        -|      -|     345|      -|
|Total            |       98|      4|   14287|  60845|
|Available        |      280|    220|  106400|  53200|
|Utilization (%)  |       35|      1|      13|    114|


***
#### 6. + ARRAY_PARTITION

```XML
<?xml version="1.0" encoding="UTF-8"?>
<est:Report xmi:version="2.0" xmlns:xmi="http://www.omg.org/XMI" xmlns:est="http://www.xilinx.com/est">
  <graph hwLatency="458058">
    <function name="top" file="AccelSchedule.cpp" line="123"/>
  </graph>
  <resources>
    <resource name="dsp" used="4" total="220"/>
    <resource name="bram" used="89" total="140"/>
    <resource name="lut" used="108137" total="53200"/>
    <resource name="ff" used="58207" total="106400"/>
  </resources>
</est:Report>
```


+ Timing (ns): 

|  Clock | Target| Estimated| Uncertainty|
|-------:|------:|---------:|-----------:|
|ap_clk  |  10.00|      9.63|        2.70|


+ Latency (clock cycles): 

|    Latency | |   Interval | | Pipeline|
|-----:|------:|-----:|------:|--------:|
|  min |  max  |  min |  max  |   Type  |
|  4775|  42212|  4775|  42212|   none  |


* Utilization Estimates

|       Name      | BRAM_18K| DSP48E|   FF   |  LUT  |
|:---------------:|--------:|------:|-------:|------:|
|DSP              |        -|      1|       -|      -|
|Expression       |        -|      -|       0|   1262|
|FIFO             |        -|      -|       -|      -|
|Instance         |       64|      3|   35374|  89083|
|Memory           |       50|      -|       0|      0|
|Multiplexer      |        -|      -|       -|    964|
|Register         |        -|      -|     441|      -|
|Total            |      114|      4|   35815|  91309|
|Available        |      280|    220|  106400|  53200|
|Utilization (%)  |       40|      1|      33|    171|


***
#### 7. SYNTHESIS RESULT

- SDSoC / Vivado 2017.4
- Clock: 100 [MHz]

|Resource|Utilization|Available|Utilization %|
|:------:|----------:|--------:|------------:|
|LUT	   |      32547|	  53200|      	61.18|
|LUTRAM  |	      635|	  17400|	       3.65|
|FF      |	    36747|	 106400|	      34.54|
|BRAM    |	       77|	    140|	      55.00|
|DSP     |	        4|	    220|	       1.82|
|BUFG    |	        3|	     32|	       9.38|
|MMCM    |   	      1|	      4|	      25.00|
