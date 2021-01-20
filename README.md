# Technical Indicators and GRU/LSTM to Predict Stock price
TECHNICAL indicators are available at large numbers and used mostly by stock traders. Most indicators have user-defined variables which allow traders to adapt key inputs such as look-back period which us how much historical data will be used to form the calculations to suit their needs. We will use some of the indicators to create features in the existing data set. Applying these features, we will see if we can predict the future price of a particular stock.
We will use Gated Recurrent Unit (GRU) and Long Short-Term Memory (LSTM) of recurrent units to compare their performance. LSTM is well established on sequence-based tasks with long-term dependencies, and GRU is a new addition in the field of machine learning which is an improvised version of Recurrent Neural Network(RNN). I found this article is quite interesting to know more about these two network architecture.
There are some similarities and differences between GRU and LSTM.

## Similarities
Both the network have additive component from t to t + 1; new content is added on the top of existing content.
Both addresses vanishing and exploding gradient issue
The update gate in GRU and forget gate in LSTM takes the linear sum between the existing state and the newly computed state

## Differences
GRU has two gates, reset and update gates compared to LSTM has three gates, input, forget and output. GRU does not have an output gate like LSTM. Update gate in GRU does the work of input and forget gate of LSTM.
GRU is computationally more efficient considering fewer parameters and need less data to generalize.
LSTM maintains an internal memory state cell, while GRU does not have a separate memory cell
GRU does not have any mechanism to control the degree to which its state or memory content is exposed, but exposes the whole state or memory content each time. LSTM can control how much memory content it wants to expose.
