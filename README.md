# CPU Scheduling Visualizer

This project provides C++ implementations and visualizations for a variety of CPU scheduling algorithms. The supported algorithms include First Come First Serve (FCFS), Round Robin (RR),Shortest Remaining Time (SRT),Aging.

## Table of Contents

- [Overview](#overview)
- [Algorithms](#algorithms)
  - [FCFS](#fcfs)
  - [Round Robin (RR)](#round-robin-rr)
  - [SRT](#srt)
  - [Aging](#aging)
- [Input Format](#input-format)

## Overview

This tool is designed to help users understand and analyze the behavior of different CPU scheduling strategies. It can be used for both educational and experimental purposes.

## Algorithms

### FCFS

First Come First Serve (FCFS) schedules processes in the order they arrive. It is simple and non-preemptive, but can result in long waiting times for short processes if a long process arrives first.

### Round Robin (RR)

Round Robin divides CPU time into fixed or variable time slices (quanta) and cycles through processes in the ready queue. Each process receives a time slice in turn, which helps prevent starvation but may increase context switching overhead.


### SRT

Shortest Remaining Time (SRT) is a preemptive version of SPN. If a new process arrives with a shorter remaining time than the currently running process, it preempts the CPU.


### Aging

Aging is used to prevent starvation by gradually increasing the priority of waiting processes. Over time, even low-priority processes will get CPU time.

## Input Format

- **Line 1:** Mode of operation: `"trace"` or `"stats"`
- **Line 2:** Comma-separated list of scheduling algorithms and their parameters (e.g., `2-4` for RR with quantum 4, `8-1` for Aging with quantum 1). Algorithms are numbered as follows:
  1. FCFS
  2. RR
  3. SRT
  4. Aging
- **Line 3:** Integer specifying the simulation end time.
- **Line 4:** Number of processes.
- **Line 5 onward:** Each process on a new line. For algorithms 1–7, format is:
    - Process Name, Arrival Time, Service Time

  For Aging (algorithm 4), format is:
    - Process Name, Arrival Time, Priority

Processes should be listed in order of arrival. If two processes arrive at the same time, the one with lower priority is listed first.

> For detailed examples, see the [testcases](https://github.com/amberpurwar636/C-Scheduling-algo-Visualizer/tree/main/testcases) directory.

# How to run in your machine
1) just navigate to your folder and compile g++ -c main.cpp       # Compiles to main.o
                                            g++ -o lab4 main.o

2) Now for ex-you want to try for 1st scheduling algorithm,then compile 
                                                                   Get-Content.\testcases\01a-input.txt |\lab4 
3) you will see the output compare it with the output file for required scheduling algorithm.                                                             


