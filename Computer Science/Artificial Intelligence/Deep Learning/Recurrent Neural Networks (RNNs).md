# Recurrent Neural Networks

## Introduction
Recurrent Neural Networks (RNNs) are a class of artificial neural networks designed for sequential data processing. Unlike traditional feedforward networks, RNNs have connections that form directed cycles, allowing them to maintain a memory of previous inputs in their internal state. This memory enables RNNs to capture temporal dependencies and patterns in sequential data.

## Basic Architecture
### 1. **Recurrent Connections:**
   - **Looping Connections:** Connections that allow information to persist over time.
   - **Hidden State:** Represents the network's memory of previous inputs.

### 2. **Time Unrolling:**
   - **Representation:** RNNs are often visualized as unrolled through time to illustrate the sequential nature of computations.
   - **Multiple Time Steps:** Each time step corresponds to one element in the input sequence.

## RNN Cell
### 1. **Inputs:**
   - **Current Input:**
     - Input at the current time step.
   - **Previous Hidden State:**
     - Hidden state from the previous time step.

### 2. **Parameters:**
   - **Weight Matrices:**
     - Parameters shared across all time steps.
   - **Bias Terms:**
     - Adjustments applied at each time step.

### 3. **Equations:**
   - **Hidden State Update:**
     - ht​=activation(Whh​⋅ht−1​+Wxh​⋅xt​+bh​)
   - **Output Calculation:**
     - yt​=activation(Why​⋅ht​+by​)

## Training RNNs
### 1. **Backpropagation Through Time (BPTT):**
   - **Idea:** Extend backpropagation to handle sequential data by unfolding the network through time.
   - **Challenges:** Vanishing and exploding gradient problems.

### 2. **Gradient Clipping:**
   - **Technique:** Limit the size of gradients during training to mitigate exploding gradients.

## Types of RNNs
### 1. **Vanilla RNNs:**
   - **Architecture:** Simple recurrent connections.
   - **Issues:** Prone to vanishing gradient problem.

### 2. **Long Short-Term Memory (LSTM):**
   - **Architecture:** Incorporates memory cells and gating mechanisms.
   - **Advantages:** Mitigates vanishing gradient problem, better at capturing long-term dependencies.

### 3. **Gated Recurrent Unit (GRU):**
   - **Architecture:** Simplified version of LSTM with fewer parameters.
   - **Advantages:** Similar performance to LSTM with reduced complexity.

## Applications
### 1. **Natural Language Processing (NLP):**
   - **Tasks:** Language modeling, machine translation, sentiment analysis.

### 2. **Time Series Prediction:**
   - **Applications:** Stock price prediction, weather forecasting.

### 3. **Speech Recognition:**
   - **Tasks:** Phoneme recognition, speech-to-text conversion.

### 4. **Video Analysis:**
   - **Applications:** Action recognition, video captioning.

## Challenges and Limitations
### 1. **Vanishing Gradient:**
   - **Issue:** Difficulty in learning long-term dependencies.
   - **Solutions:** LSTM and GRU architectures.

### 2. **Limited Context:**
   - **Challenge:** RNNs may struggle with capturing dependencies over very long sequences.

### 3. **Computational Complexity:**
   - **Issue:** Training RNNs can be computationally expensive.
