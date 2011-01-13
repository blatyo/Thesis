# User Trust on the Web

## Introduction
1. Describe what a CAPTCHA is.
2. Describe evolution of CAPTCHAs
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
        * Usable (Provides noticeable benefit to the user)
    * Hypothesis
        * It is possible to increase usability and maintain security while decreasing the occurrence of CAPTCHAs with the use of feedback filtering and clustering.
7. Describe the paper layout and how it will address the compromise.

## Related Works
1. Describe CAPTCHAs in more depth.
    * Types
    * Smarter AI causing common type to be more complicated to solve.
    * Usability of CAPTCHAs being addressed in other ways. (Video CAPTCHA, Drag-and-drop tests)
2. Describe work done in reputation systems, referral systems, and collaborative filtering/sanctioning.
    * Distributed vs Cetralized
    * Methods of generating reputation (Summation/Average, Bayesian, Discrete Trust Models, Belief Models, Fuzzy Models, Flow Models)
    * Clustering/Top N Items
        * Similarity Measures
    * Attacks on these types of systems
3. Methods for protecting against strategic oscillation.

## Functional Specification
1. Talk about registering users
2. Talk about registering a site and confirming ownership
3. Talk about API

## Design Specification
1. Describe model where one site takes averages for each users performance.
    1. Introduce sessions as a way to better handle calculating scores to account for human error.
        * Why is a session necessary?
        * How to calculate it.
    2. Introduce malicious user
        1. Describe the goal of the malicious user.
        2. Describe how malicious user would attempt to attack the system and how it can be countered.
            * Describe how average doesn't represent true behavior. (Most recent more important)
            * Introduce PID Controllers and TrustGaurd and describe what properties make them useful. (Good reputation hard to obtain, detect fluctuations in behavior)
            * Explain problems with TrustGaurd for use with UserTrust and how they can remedied.
                * Degrading trust between CAPTCHAs (should increase briefly)
                * Consistent intervals (May need different fading memory function)
    3. Introduce malicious site and why user reputations can't be simple averages
        1. Describe the goal of the malicious site.
        2. Describe the attack of the malicous site and how it will be countered.
            * Describe method of verifying CAPTCHA transactions
            * Describe method for clustering sites using similarity of users.
            * Describe how clusters are used to calculate reputation and how reputation can be different for the same user on different sites.
    4. Talk about a model for efficient computation
        1. Lazy computing successful CAPTCHAs
        2. Immediate computing of failed CAPTCHAs
        3. Storing computed values
        4. Lazy computing similarities (May be beneficial for detecting a user who has changed behavior)
        5. Talk about storage structure for data
    5. Talk about how system is to be evaluated
        1. Simulation of many sites
            * Good sites modeling
            * Malicious sites modeling
        2. Simulation of many users
            * Good user modeling (Techie, Grandpa, Kid, etc...)
            * Bad user modeling (Alternating behavior, etc...)

## Schedule
TBD