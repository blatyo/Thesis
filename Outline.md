# User Trust on the Web

## Introduction
1. Describe how the goal of websites is to increase usage.
2. Describe how trying this goal can lead to different approaches to fighting against each other.
    * Usability
        * Systems that are easy to use will be used more frequently.
    * Security
        * CAPTCHA prevents spammy messages and content.
3. Describe the necessity for these features to exist.
4. Describe how a compromise is necessary.
5. Describe a brief overview of the proposed system.
6. State goals and hypothesis.
    * Goals
        * Open (Kerckhos' Principle)
        * Secure (Resistant against malicious users and sites)
        * Performant (Able to handle the computation of user scores)
        * TODO: anything else?
    * Hypothesis
        * It is possible to increase usability and maintain security while decreasing the occurrence of CAPTCHAs with the use of feedback filtering and clustering.
7. Describe the paper layout and how it will address the compromise.

## Background
1. Describe CAPTCHAs.
    * Definition and common type.
    * Smarter AI causing common type to be more complicated to solve.
    * Usability of CAPTCHAs being addressed in other ways.
2. Describe work done in reputation systems, referral systems, and collaborative filtering.
    * TODO: more in depth here
3. TODO: Anything else?

## Functional Specification
1. Describe model where one site takes averages for each users performance.
    1. Introduce sessions as a way to better handle calculating scores to account for human error.
        * Why is a session necessary?
        * How to calculate it.
    2. Introduce malicious user
        1. Describe the goal of the malicious user.
        2. Describe how malicious user would attempt to attack the system and how it can be countered.
            * Describe how average doesn't represent true behavior. (Most recent more important)
            * Introduce 


## Design Specification
