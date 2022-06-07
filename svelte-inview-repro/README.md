repro for https://github.com/maciekgrzybek/svelte-inview/issues/19#issuecomment-1147661009

All issues appear in inviewComponent.svelte.

line 10 throws the error
```
Binding element 'detail' implicitly has an 'any' type.ts(7031)
```

line 17 throws the error 
```
Type '({ detail }: { detail: any; }) => void' is not assignable to type 'FormEventHandler<HTMLElement>'.
Types of parameters '__0' and 'event' are incompatible.
Property 'detail' is missing in type 'Event & { currentTarget: EventTarget & HTMLElement; }' but required in type '{ detail: any; }'.ts(2322)
```

line 18 throws the error
```
'inView' is not definedsvelte(missing-declaration)
```

I used the code from the animation sample in the packages readme.