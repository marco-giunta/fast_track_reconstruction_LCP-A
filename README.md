# Fast track reconstruction in drift tube detectors (LCP-A exam)

This repository contains a backup of the pull request with the final version of the assignment delivery.

The project is divided in 4 parts according to the following schema:
- Part 0: Preprocessing (auth.: Lorenzo Borella)
- Part 1: Time pedestal computation, ambiguity not resolved (auth: Mattia Ceravolo)
- Part 2: Ambiguity resolution & final trajectory estimate (auth: Samuele Pio Lipani)
- Part 3: Profiling, optimization & refactoring of all of the above (auth: Marco Giunta)

The TL;DR of the whole pipeline is the following: we discard clearly unphysical events (i.e. impossibly curved trajectories), compute the time pedestal based on the ion drift speed inside the detectors, then estimate the trajectory using a $\chi^2$ based approach to select the "straightest" (hence most physical) possible trajectory, which is itself computed using linear regression.
