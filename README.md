
## @kilt/watchdir

### Install
``` sh
npm i -D @kilt/watchdir
```

### Running CLI
``` sh
npx watchdir ./src \
  --when "{,**/}*.js" "make js" \
  --when "{,**/}*.sass" "make css" \
  --run "echo 'all when detected has finished'"
```

### API JavaScript
``` js
import WatchDir from '@kilt/watchdir'

new WatchDir('./src')
  .when('{,**/}*.js', () => console.log('js files changed') )
  .when('{,**/}*.sass', () => console.log('sass files changed') )
  .run( () => console.log('all when detected has finished) )

```
