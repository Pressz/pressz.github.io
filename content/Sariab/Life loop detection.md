# Tayyebi Loop of Misery

In some periods of time,
human is kept accustomed by enviroment
containing media, friends, lifestyle, etc...

If it was possible to create
a list of all enviroment elements
known by a tuple of id and other properties,
then it will be possible to generate array 'a'
which is representing peer to peer accustomization of elements mentioned.

> e.g->
>
> Human H has following life style
>
> enviroment_elements:
>   - breakfast, 1 hours/day, morning, egg and milk
>   - news, 2 hours/day, morning, bbc
>   - university, 4 hours/day, noon, mathematics
>   - gym, 1 hours/day, afternoon, pool
>   - chat, 2 hours/day, night, politics
>
> H is accustomed by the current lifestlye
> so 'a' array will be generated as following:
>
> [True, True, True, True, True]
>
> H will not face any new optional and selective event until
> updating the daily program with new friends
>
> enviroment elements (new):
> chat, 3 hours/day, night, art-politics
>
> H is not already accustomed with new enviroment elements
> so 'a' array will be generated as following:\
>
> [True, True, True, True, False]
> 
> then H has the chance to explore more out of life
> using explore() function.

explore() uses X.
X will be true if H is accustomed by enviroment;
and it will be false even if there is an element which isn't accustomed yet
so the busy loop will pass.

## Algorithm

<pre>
<code>
a = [True, True, True, False, True, True]
X = lambda n : a[n] if n < 1 else X(n-1) and a[n]

def explore ():
    
    .
    . EACH HUMAN STRATEGY OF LIFE
    . UPDATING a
    . UPDATING enviroment_elements
    .

    while X(len(a) - 1):
        continue
    explore()

explore()
<code>
</pre>