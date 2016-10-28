# breachbay
A collaborative effort between arc4n4 and friends to create and maintain the breachbay service within h a c k m u d.

Breachbay will have three seperate parts, all connected via the database:

 > breachbay.mark { t:#s.user.loc } : A script that will "mark" a breached user, writing the most recent bits of their access_log (not including the breached user, and any repeated info), transactions (above 10KGC), and balance to the database. If a contract offers additional money beyond the base payout per user (TBD), then the script will give that amount either in addition to, or in place of the base payout.
 
 > breachbay.find {  } : A script that will search through the database for breached users. It *may* output a list of users that, when entered into params, along with a `confirm: true, script: #s.accts.xfer_gc_to` for payment, will output the latest information written by **breachbay.mark**
 
 > breachbay.board {  } : A script that will contain database entries for contracts put out. The idea here is that the user putting out the contract will remain anonymous, as well as the user that completes it and turns it in. This does two things. First, it funnels everything through here, making us important, and second, it allows for a completely anonymous environment for users to post jobs.
