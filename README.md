JPMC Sentiment Analysis

- Using price data from 2019-01-01 to 2024-12-31, to compare it with
  Jamie Dimon's statements in the earning call transcripts.

I will collect the earning transcripts then run sentiment analysis with VADER
then map the sentiment to price movement. The findings should reveal the behavior of the stock with respect to the managements reports. 

Essentially building a language based early warning system for banking sector health. 

05-24-2026
Exported the stock data from 2019-01-01 to 2024-12-31 and visualized it using pyplot.

Graph Analysis:
The graph shows a sharp dip during first covid outbreak, then some upward momentum followed by a stabalization period, followed by another dip during late 2022, then strong upward momentum, doubling the stock price by the end of 2024. 

05-25-26
Extracted text from Q1Y20, Q3Y20, Q1Y22, Q3Y22, and Q1Y23 earning calls transcripts. 

I tried running VADER on each transcript which gave me a compound score of 1, which means a totally positive sentiment, the sentiment scores for categories like neg, neutral, and positive were very consistent across all the transcripts. Makes sense because the management isn't supposed to tell you anything actually, they're just meant to be vague and optimistic, which is why VADER picks up a net positive. 

Taking the compound scores for each line and averaging them resulted in a much lower score. 

Average Compound scores:
Q1Y20 - 0.1381
Q3Y20 - 0.1450
Q1Y22 - 0.1372
Q3Y22 - 0.1408
Q1Y23 - 0.1266

The compound score was the lowest for Q1Y23, which means the most cautious the managment has been in their earnings transcripts out of all 5. Interestingly enough, the bull run for JPMC started right after this quarter and ended up doubling the stock price by the end of 2024.

This means that the sentiment analysis diverged from the actual price history.

05-26-26
I plotted the sentiment analysis scores and the price history vs time and the two graphs diverge, the analysis scores predict a steady downward momentum after 2020 Q3 while the stock price actually goes up. 

The sentiment analysis was performed on the entire transcript, which included statements from multiple people. To get the company specific signals, I will capture Jamie Dimon's text in the transcript and perform the sentiment analysis on them specifically. 

Average Compound Scoreds for Jamie Dimon's sections
Q1 2020:  mean=0.0435, sentences=98
Q3 2020:  mean=0.0611, sentences=110
Q1 2022:  mean=0.0764, sentences=159
Q3 2022:  mean=0.1446, sentences=406
Q1 2023:  mean=0.1177, sentences=425

The sentiment line for dimon's scores moves much more closely to the priceline, the line is faulty towards Q1 2023 part but it tracks the overall much better. 

05-27-26
Adding more transcripts for better signal analysis. 

I ran the signal against the price for managment and for Dimon alone, the charts were in sync with the signal much more than with the 5 transcripts, Dimon's signals were more accurate and closer to the actual trend, management's were more inflated. 