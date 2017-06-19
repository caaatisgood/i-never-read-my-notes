`q` to quit `git log`

find overtime commits so I can cc to renee faster
`git log --pretty="%cd %s" --author=imrobinized --after="2017-05-21" --before="2017-06-21" --date=iso | grep -E "([19]:[3-5][0-9]:|[2][0-3]:[0-5][0-9]:)"`