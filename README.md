# Modeling-of-4-bit-Flash-ADC-and-4-bit-DAC
This project shows how to model a 4-bit flash ADC and a 4-bit DAC using ideal components. Used vdc, vpulse, vcvs, switch, res, cap, vccs to construct the 4-bit ADC based on the flash architecture. Models are built in Cadence using ideal components & VerilogA blocks, & Analysis is done on Matlab.

## Ideal Comparator
![Ideal_Comparator_w](https://user-images.githubusercontent.com/27668656/56461531-6fce0780-6369-11e9-8ece-db9b83139679.png)

## Ideal Clocked Comparator
![Ideal_ClockedComparator_w](https://user-images.githubusercontent.com/27668656/56461535-84aa9b00-6369-11e9-95f0-f76a683c3097.png)

## 4-bit Flash ADC
1- To create the Thermometer-Code Output, ((2^4)-1) Comparators & (2^4) voltage levels created by the resistive ladder are used.
![Ideal_LadderAndComparators_w](https://user-images.githubusercontent.com/27668656/56461733-7d38c100-636c-11e9-9d88-a3d5cf3bd6d2.png)
2- To Convert the Thermometer-Code to a Binary-Code Output, a ROM Encoder is placed after the Comparators.
![Ideal_ThermoToBinary_w](https://user-images.githubusercontent.com/27668656/56461770-fcc69000-636c-11e9-8b2d-fd44cffdd55b.png)
3- The whole flash ADC: 
![Ideal_FlashADC_w](https://user-images.githubusercontent.com/27668656/56461813-bd4c7380-636d-11e9-91bb-5e506163920e.png)

## 4-bit DAC
![Ideal_DAC_4bit_w](https://user-images.githubusercontent.com/27668656/56461819-d1907080-636d-11e9-9ae6-13981bbc0327.png)

## System Testbench
![TB_Flash_Ideal_w](https://user-images.githubusercontent.com/27668656/56461821-da814200-636d-11e9-87e4-d789983f1e73.png)

-> Using VerilogA blocks: <br/>
![VerilogA_Testbench_w](https://user-images.githubusercontent.com/27668656/56461829-f4bb2000-636d-11e9-85bd-66c7d15dd35a.png)
*****************
## To analyze the output results:
- Using Cadence:<br/>
Select the transient signal of the DAC's output, then use the "dft" & "dB20" functions in the ADE calculator to plot the output FFT spectrum.<br/>
https://drive.google.com/open?id=1P0Qo3bQ7QQucbzPnD_u01404rpjmt8zj <br/>
- Using Matlab:<br/>
Sample the transient signal of the DAC's output by using the "sample" function in the ADE calculator, then save tha samples in a CSV file, then Run the Matlab code on the CSV data.<br/>
https://drive.google.com/file/d/1yapHM566FUtoERnFrU_xc2nd3FOF-ETe/view <br/>

*****************
### References:
My project on google drive:<br/>
https://drive.google.com/drive/folders/1W9ip4MpMZNf3IQsoFQkhgg6QaUya4Yp4 <br/>
EE288 Lecture Notes:<br/>
https://drive.google.com/drive/folders/12Qqfw_TX1i7dvVVYXksaSdHV4gth1OD5 <br/>
Videos on how to create VerilogA blocks for ADCs:
https://drive.google.com/drive/folders/1GAobRzzFTkD6ywqSdDJUsO5g2C06hh_i <br/>
https://www.youtube.com/channel/UC7jwESeWKLcRbtxHwFS3A7Q/videos 
