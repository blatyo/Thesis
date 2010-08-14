# User Trust on the Web - Proposal

- [Preproposal](http://github.com/blatyo/Thesis/blob/master/Preproposal.md)

## Summary
A CAPTCHA is a test which uses a difficult artificial intelligence problem to distinguish between a human and a computer. This sort of test is useful for defending various types of systems from automated usage [1]. Take for example the website Digg, which allows its users to submit links to content they like and vote for their favorite links. Links that have a high number of votes are promoted to the front page and receive a lot of views. As a result, it would be desirable for a malicious user to automate the creation of accounts, submission of links, and voting for those links to promote traffic to the website of the malicious user. In all three of these cases a CAPTCHA could be used to prevent the malicious user from automating these tasks and circumventing the democratic nature of Digg.

Using a CAPTCHA is problematic though, because it is cumbersome for a user to solve [2, 3]. An ideal website would always show a CAPTCHA to a computer and never show a CAPTCHA to a human user. However, it is not possible to know in advance if a user is a human or a computer. Therefore, it is necessary to settle for an option that is less than ideal. There are three options to address when to show CAPTCHAs. The first is to always show a CAPTCHA to the user. However, this option has the drawback that it always shows a CAPTCHA to the human user. The second option is to never show a CAPTCHA. The problem with this is that it ignores the goal to always show an automated user a CAPTCHA. The third option is to make an intelligent guess about when it is appropriate to show a CAPTCHA. This option is much better than the previous two, because it considers both goals.

Even though this third option is better, it is more complex and has problems that must be solved before it can be used. The first problem is that to make an intelligent guess it is necessary to track additional information about the user. For this information to be useful it must be a strong predictor of the future performance of a user passing a CAPTCHA. If the data can be used to determine how a user would perform on a CAPTCHA then it is possible to intelligently guess whether a CAPTCHA should or should not be shown. Past performance on CAPTCHAs works very well in this case, because a user with a history of passing CAPTCHAs should be able to pass another. Another problem is that currently, only the website showing the CAPTCHA knows whether the user passed or not. Since every website is autonomous there needs to be a way to incentivize websites to provide the information and also some way to determine whether the information provided is trustworthy. The incentivisation is achieved because providing the information increases the ability to determine whether to show a CAPTCHA or not. The trustworthiness of the data provided is much harder to achieve since it is unknown whether the website providing it is trustworthy. Therefore, it is necessary to assign a credibility rating to web sites and weigh the history provided by credible sources more than less credible ones [4, 5]. Various ways to weigh data providers are explored in [4], [6], [7], [8], [9], and [10]. Finally, there is the problem of a user changing behavior. For example, it would be possible for a user to set up an account, build up a history of passing CAPTCHAs, and then give the account to a computer to use. There needs to be measures taken to protect against this sort of situation, such as periodical checks to ensure the user is still trustworthy.

To solve the problems described, I propose a system called UserTrust. UserTrust is comprised of two components: TrustHistory and TrustScorer. TrustHistory is a set of tuples containing the results of a CAPTCHA test, a timestamp of when the test was completed, a reference to the user who completed the test, and a reference to the site the test was given on. TrustScorer is an algorithm that uses TrustHistory to generate a TrustRating for users. TrustScorer will use exogenous discounting [11] to filter out false feedback from malicious websites. Like [12], it will use a cost model to detect strategic changes in behavior of both users and websites. The difference between the work done in [12] and UserTrust will be the application of these methods to a centralized trust referral system as opposed to a peer-to-peer reputation system. Web service components will be created to allow websites to provide TrustHistory data and access the TrustRating of users. I will perform a simulation based analysis of the system to show that UserTrust is able to discern a human from a computer better than always showing a CAPTCHA, never showing a CAPTCHA, and random guessing. I will also conduct a literature review of existing works to identify other attacks on a repuation system, methods of defending against those attacks, and ways to evaluate the correctness and validity of a reputation system.

## Overview

## Functional Specification

## Design Specification

## Reference
[1] Ahn, L., Blum, M., Hopper, N., and Langford, J. 2003. CAPTCHA: Using Hard AI Problems for Security. In Proceedings of the International Conference on the Theory and Applications of Cryptographic Techniques, Warsaw, Poland, May 2003. Springer Berlin / Heidelberg, 2003.

[2] Yan, J. and El Ahmad, A. S. 2008. Usability of CAPTCHAs or usability issues in CAPTCHA design. In Proceedings of the 4th Symposium on Usable Privacy and Security (Pittsburgh, Pennsylvania, July 23 - 25, 2008). SOUPS '08, vol. 337. ACM, New York, NY, 44-52. DOI= http://doi.acm.org/10.1145/1408664.1408671

[3] Ben-Asher, N., Meyer, J., Moller, S., and Englert, R. 2009. An Experimental System for Studying the Tradeoff  between Usability and Security. In Proceedings of the International Conference on Availability, Reliability, and Security, Fukuoka, Japan, March 2009. International Conference on Availability, Reliability, and Security, 2009.

[4] Malik, Z. and Bouguettaya, A. 2009. RATEWeb: Reputation Assessment for Trust Establishment among Web services. The VLDB Journal 18, 4 (Aug. 2009), 885-911. DOI= http://dx.doi.org/10.1007/s00778-009-0138-1

[5] Tennenholtz, M. 2004. Reputation systems: an axiomatic approach. In Proceedings of the 20th Conference on Uncertainty in Artificial intelligence (Banff, Canada, July 07 - 11, 2004). ACM International Conference Proceeding Series, vol. 70. AUAI Press, Arlington, Virginia, 544-551.

[6] Delgado, J., Ishii, N.: Memory-based weighted-majority prediction for recommender systems. In: ACM SIGIR '99 Workshop on Recommender Systems: Algorithms and Evaluation (1999).

[7] Huynh, T. D., Jennings, N. R., and Shadbolt, N. R. 2006. Certified reputation: how an agent can trust a stranger. InProceedings of the Fifth international Joint Conference on Autonomous Agents and Multiagent Systems (Hakodate, Japan, May 08 - 12, 2006). AAMAS '06. ACM, New York, NY, 1217-1224. DOI= http://doi.acm.org/10.1145/1160633.1160854

[8] Park, S., Liu, L., Pu, C., Srivatsa, M., and Zhang, J. 2005. Resilient Trust Management for Web Service Integration. InProceedings of the IEEE international Conference on Web Services (July 11 - 15, 2005). ICWS. IEEE Computer Society, Washington, DC, 499-506. DOI= http://dx.doi.org/10.1109/ICWS.2005.99

[9] Sonnek, J. D. and Weissman, J. B. 2005. A Quantitative Comparison of Reputation Systems in the Grid. In Proceedings of the 6th IEEE/ACM international Workshop on Grid Computing (November 13 - 14, 2005). International Conference on Grid Computing. IEEE Computer Society, Washington, DC, 242-249. DOI= http://dx.doi.org/10.1109/GRID.2005.1542748

[10] 2004. PeerTrust: Supporting Reputation-Based Trust for Peer-to-Peer Electronic Communities. IEEE Trans. on Knowl. and Data Eng. 16, 7 (Jul. 2004), 843-857. DOI= http://dx.doi.org/10.1109/TKDE.2004.1318566

[11] Whitby, A., Josang, A., Indulska, J.: Filtering out unfair ratings in bayesian reputation systems. Icfain J. Manage. Res. 4(2), 48-64 (2005).

[12] Srivatsa, M., Xiong, L., and Liu, L. 2005. TrustGuard: countering vulnerabilities in reputation management for decentralized overlay networks. In Proceedings of the 14th international Conference on World Wide Web (Chiba, Japan, May 10 - 14, 2005). WWW '05. ACM, New York, NY, 422-431. DOI= http://doi.acm.org/10.1145/1060745.1060808

## Draft Table of Contents

## Schedule