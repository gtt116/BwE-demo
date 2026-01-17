# BBR Adaptation Dashboard

An interactive visualization of the BBR (Bottleneck Bandwidth and Round-trip propagation time) congestion control algorithm.

## Overview

This dashboard simulates the behavior of Google's BBR algorithm, which dynamically adapts to network conditions to maximize throughput while minimizing latency. The visualization shows how BBR responds to changes in link capacity and network conditions.

## Features

- Real-time visualization of BBR's key metrics:
  - **Physical Link Capacity** (grey dashed line): The actual network capacity
  - **BBR Bottleneck Bandwidth Estimate** (green line): BBR's estimate of available bandwidth
  - **Pacing Rate** (blue line): Actual sending rate with ProbeBW pulsing
- Interactive controls for adjusting link bandwidth and noise levels
- Instant capacity drop simulation to observe BBR's reaction
- Adjustable simulation speed

## How It Works

- The **Windowed Max Filter** (green line) represents BBR's bandwidth estimation with memory effects
- The **ProbeBW Pulse** (blue line) constantly probes for more bandwidth with up/down cycles (1.25x and 0.75x)
- BBR maintains the pacing rate close to the estimated bottleneck bandwidth to avoid bufferbloat

## Controls

- **Link Bandwidth**: Adjust the physical capacity of the simulated network link
- **Noise (Jitter)**: Add random variation to simulate network jitter
- **Sim Speed**: Control the speed of the simulation
- **Instant 50% Capacity Drop**: Simulate a sudden reduction in network capacity
- **Reset History**: Clear the visualization history

## Usage

Simply open `index.html` in any modern browser to start exploring BBR behavior under different network conditions.