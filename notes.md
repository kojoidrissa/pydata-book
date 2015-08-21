#Notes or ideas from "Python for Data Analysis"
-  pg 26: I'm trying to use Regex to only pull review data that matches certain patterns. I'm doing this the wrong way, but I should figure out how to do it. `re.match` didn't work either
    <code>
    In [60]:import re
    In [78]:mean_ratings.index[1]
    Out[78]:'10 Things I Hate About You (1999)'
    In [82]:re.search('10', mean_ratings.index[1]) == True
    Out[82]:False
    In [85]:
    for i in mean_ratings.index:
        if re.match('10', mean_ratings.index[i]):
            print mean_ratings.index[i]

    IndexError: only integers, slices (`:`), ellipsis (`...`), numpy.newaxis (`None`) and integer or boolean arrays are valid indices
    </code>
    
    -  THIS works
        <pre>
        for i in mean_ratings.index:
            if re.match('10', i):
                print i
        </pre>

-  reversing a DataFrame? Then taking the first 15. I've never seen this 'reversing' syntax before: `sorted_by_diff[::-1][:15]`
-  s