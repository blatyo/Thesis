# Schedule

## Proposal _Mon, Jan 3 - Fri, Jan 21_ (15 days)

* Introduction _Mon, Jan 3 - Wed, Jan 5_ (3 days)
    * _Mon, Jan 3_ Find news on CAPTCHAs being broken
    * _Mon, Jan 3_ Find papers on CAPTCHAs (increasing difficulty, increasing usability)
    * _Mon, Jan 3_ Collect papers research is based on
    * _Tue, Jan 4 - Wed, Jan 5_ Write
* Related Works _Wed, Jan 5 - Tue, Jan 11_ (5 days)
    * Find papers on:
        * _Mon, Jan 3_ different types of CAPTCHAs,
        * _Wed, Jan 5_ distributed vs centralized,
        * _Done_ reputation,
        * _Thu, Jan 6_ clustering,
        * _Wed, Jan 5_ similarity measures,
        * _Wed, Jan 5_ filtering feedback,
        * _Done_ attacks
    * _Fri, Jan 7_ Collect papers for reputation, clustering, filtering feedback, attacks
    * _Fri, Jan 7 - Tue, Jan 11_ Write
* Functional Specification  (2 days)
    * _Wed, Jan 12_ Find papers for security features used if possible (salted hash passwords, http basic auth, ssl, site ownership verification)
    * _Wed, Jan 12 - Thu, Jan 13_ Write
* Design Specification _Fri, Jan 14 -_ (5 days)
    * _Fri, Jan 14_ Collect papers research is based on
    * _Fri, Jan 14 - Thu, Jan 20_ Write
* Abstract _Fri, Jan 21_ (1 day)

## Development _Fri, Jan 21 - Wed, Feb 9_ (14 days)

* Site _Done_ (0 days)
    * _Done_ User registration
    * _Done_ Site registration
    * _Done_ Site ownership confirmation
* Algorithm _Fri, Jan 21 - Thu, Feb 3_ (10 days)
    * _Fri, Jan 21 - Tue, Jan 25_ Filtering
    * _Wed, Jan 26 - Thu, Feb 3_ Clustering
        * _Wed, Jan 26 - Thu, Jan 27_ Similarity
* API _Fri, Feb 4_ (1 day)
    * _Fri, Feb 4_ --> Request user TrustScore    <-- Respond with TrustScore
    * _Fri, Feb 4_ --> Request if CAPTCHA correct <-- Respond with correctness (Simulated)
* Simulation
    * _Fri, Feb 4 - Mon, Feb 7_ TueCreate user profiles (Grandpa, Strategic user)
        * Percent of time able to answer correctly
        * Time between CAPTCHAs
        * Number of sites used
    * _Mon, Feb 7_Create population profiles
        * Distribution of user profiles
    * _Tue, Feb 8_Create runner that goes through cycles of adding users, sites, and testing users
    * _Tue, Feb 8 - Web, Feb 9_ Track performance of user profiles
        * Number of times could have been shown a CAPTCHA
        * Number of times shown a CAPTCHA
        * Number of times CAPTCHA passed
    * _Wed, Feb 9_ Run simulation

## Final Thesis

* Revisions _Thu, Feb 10 - Mon, Feb 14_ (3 days)
* Results _Tue, Feb 15 - Thu, Feb 17_ (3 days)
    * Create diagrams
* Conclusions _Fri, Feb 18 - Mon, Feb 21_ (2 days)
* Future Work (Possibly merge into conclusions) _Mon, Feb 21_ (1 day)
* Abstract _Mon, Feb 21_ (1 day)

## Defense
TODO: Look into this