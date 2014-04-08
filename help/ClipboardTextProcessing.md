### Add quotes to string (tpq)
`sed -e 's/^/\"/' | sed -e 's/$/\"/g'`
this is a test > "this is a test"


### Add parenthesis to a string (tpp)
`sed -e 's/^/(/' | sed -e 's/$/)/g'`
this is a test > (this is a test)


### Create a Slug (tps)
`sed -e 's/ /-/g' | awk '{print tolower($0)}'`
# this is a test > this-is-a-test-


### Convert to all upper case (tpu)
`tr "[:lower:]" "[:upper:]"`
this is a test > THIS IS A TEST


### Convert to all lower case (tpl)
`tr "[:upper:]" "[:lower:]"`
THIS IS A TEST > this is a test


### Remove spaces (tprs)
`sed -e 's/ //g'`
this is a test > thisisatest


### Title Case (tpt)
`tr "[:upper:]" "[:lower:]" | perl -ane ' foreach $wrd ( @F ) { print ucfirst($wrd)." "; } print "\n" ; ‘`
this is a test > This Is A Test 


### Title Case with no spaces (tpts)
`tr "[:upper:]" "[:lower:]" | perl -ane ' foreach $wrd ( @F ) { print ucfirst($wrd)." "; } print "\n" ; ' | sed -e 's/ //g'`
this is a test >ThisIsATest
