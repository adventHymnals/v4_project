## Migration

From [hymnals.yaml](https://raw.githubusercontent.com/adventHymnals/v3/gh-pages/hymnals.yaml) we copy the contents to vs code and use the regex `^(?!.*gtLink).*$\n` to match and remove all lines which are not `gtLinks`.

Then match `.*/(.*)` and replace with   `'$1',` to extract only the gtlink names (repo names). Remove the last  entry `blog pages` and create an array by adding square brackets.

Replace `-csycms` with `-v4`

Then we have the following list of hymnals:

```js
var hymnals = [
'campus-melodies-v4',
'hymns-for-the-poor-of-the-flock-v4',
'millenial-harp-v4',
'Hymns-for-Gods-Peculiar-People-v4',
'christ-in-song-v4',
'church-hymnal-v4',
'seventh-day-adventist-hymnal-v4',
'nyimbo-za-kristo-v4',
'wende-nyasaye-v4'
]
```

On second thought, convert the json to yaml

```
hymnals:
    - 'campus-melodies-v4'
    - 'hymns-for-the-poor-of-the-flock-v4'
    - 'millenial-harp-v4'
    - 'Hymns-for-Gods-Peculiar-People-v4'
    - 'christ-in-song-v4'
    - 'church-hymnal-v4'
    - 'seventh-day-adventist-hymnal-v4'
    - 'nyimbo-za-kristo-v4'
    - 'wende-nyasaye-v4'
```
