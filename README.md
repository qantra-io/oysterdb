# featherdb-redis

A Redis that is utilized with Axion functions like OysterDB.

<aside>
👉 oysterdb docker image is mandatory for this package to work.

</aside>

```jsx
const Oyster = require('oysterdb');
const oyster = new Oyster({ 
	url: "redis://127.0.0.1:6379", 
	prefix: "none" 
});
```

# OYSTER

### Example Call

```jsx
oyster.call('add_block',{
    _label: 'comments',
    _id: '12345',
    _hosts: ['school:019029'],
    _members: ['hoppies:039049'],
    fullname: 'bahi hussein abdel baset',
    lastname: 'ismail',
    label: 'vodo',
    hoppies: 'flying',
    ok: ['3', '3', '3', '123'],
    tom: {
        cort: {
            r: 0.123,
            x: 'will be deleted'
        }
    },
    experince: {
        dog_years: 154
    }
})
```

```json
{
	"_label":"comments",
	"_id":"comments:123",
	"fullname":"bahi hussein abdel baset",
	"lastname":"ismail",
	"label":"vodo",
	"hoppies":"flying",
	"ok":"["3","3","3","123"]",
	"tom":{
	"cort":{
	"r":"0.123",
	"x":"will be deleted"
	}
	},
	"experince":{
	"dog_years":"154"
	}
}
```

# HYPERVIEW