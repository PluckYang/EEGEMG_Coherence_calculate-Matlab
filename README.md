# EEGEMG_Coherence_calculate-Matlab  
【Cont_cohere.m】为主函数  
用于处理36通道的原始信号  
其中1-32通道为EEG  
33-34通道为EOG  
35-36通道为EMG，35为右脚，36为左脚  
首先原始信号会被使用【filter_2sIIR.m】函数进行滤波  
1-32EEG信号以及35-36EMG信号滤波范围为1-50HZ  
随后经过【FastICA_25】工具经行ICA处理，分离出成分占有率前十的成分，并与EOG信号比对，移除相似度大于0.5的成分  
最后将1-32EEG信号分别于35-36EMG信号进行同调性分析，并画图表示

【Cont_cohere.m】Main function  
Used to process 36 channels of raw signals  
Among them 1-32 channels are EEG  
33-34 channels are EOG  
35-36 channels are EMG, 35 is right foot, 36 is left foot  
First, the original signal will be filtered using the 【filter_2sIIR.m】 function  
1-32EEG signal and 35-36EMG signal filtering range is 1-50HZ  
Then, 【FastICA_25】 tool is used to process ICA, the top ten components with component occupancy are separated and compared with the EOG signals, to remove components with similarity greater than 0.5  
Finally, the 1-32EEG signal is analyzed for coherence with the 35-36EMG signal, and the graph is shown.  
