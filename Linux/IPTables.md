## IPtable rules

The default table "Filter" contains three chains, Input, Outout, Forward.

List all rules "sudo iptables -Lvn", NOTE the rules in a Chain are applied in order top to bottom.

List INPUT Chain "sudo iptables -L INPUT --line-numbers" line-numbers is good to use if there is a need to replace or insert a rule in the chain

INPUT Chain is for incoming port connections, (policy Accept) this will allow incomming requests based on the rules in the chain.

OUTPUT is for outgoing connections

Add rules
sudo iptables -A chain -p port -s sourceIP --dport destinationport 
using -A will append to the chain at the bottom position.
