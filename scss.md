# SCSS

# Animations

```
/// transition
@mixin x-transition ( $t: $transition, $s: 0.222s, $e: ease-out ){
    -webkit-transition: $t $s $e;
    -moz-transition:    $t $s $e;
    -ms-transition:     $t $s $e;
    -o-transition:      $t $s $e;
    transition:         $t $s $e;
}
```

```
/// Rotate
@mixin x-rotate (){ transform: rotate( 180deg ) 0.3s ease-out; }
```


# Resets

```
/// reset list
@mixin reset-list() {
  margin:0;
  padding:0;
  list-style:none;
  display:block;
  li {
    margin:0;
    padding:0;
    list-style:none;
    display:block;
  }
}
```
