# Add quotes to string (q)
sed -e 's/^/\"/' | sed -e 's/$/\"/g'
# this is a test > "this is a test"


# Add parenthesis to a string (p)
sed -e 's/^/(/' | sed -e 's/$/)/g'
# this is a test > (this is a test)


# Create a Slug (s)
sed -e 's/ /-/g' | awk '{print tolower($0)}'
# this is a test > this-is-a-test-


# Convert to all upper case (u)
tr "[:lower:]" "[:upper:]"
# this is a test > THIS IS A TEST


# Convert to all lower case (l)
tr "[:upper:]" "[:lower:]"
# THIS IS A TEST > this is a test


# Remove spaces (rs)
sed -e 's/ //g'
# this is a test > thisisatest


# Title Case (t)
tr "[:upper:]" "[:lower:]" | perl -ane ' foreach $wrd ( @F ) { print ucfirst($wrd)." "; } print "\n" ; ‘ 
# this is a test > This Is A Test 


# Title Case with no spaces (ts)
tr "[:upper:]" "[:lower:]" | perl -ane ' foreach $wrd ( @F ) { print ucfirst($wrd)." "; } print "\n" ; ' | sed -e 's/ //g'
# this is a test >ThisIsATest
