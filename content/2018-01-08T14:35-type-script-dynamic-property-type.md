Title: How to define type in type-script for dynamic property name? 
Date: 2018-01-08 14:35
Category: type-script
Tags: es6, typescript, type-script 

# Problem 😱

You would like to create type for following object with dynamic property name:

```javascript
const gallery = {
  homepage: {
    key: 'gallery-of-users',
    activeSlide: 1,
  },
  feed: {
    key: 'gallery-of-posts',
    activeSlide: 10
  }
}
```

---

# Solution 🤓

```typescript
export interface IGalleryItem {
  key: string;
  activeSlide: string;
}

export interface IGallery {
  [slideKeyWhichIsDynamic:string]: IGalleryItem;
}
```

Usage:
```
const gallery: IGallery = {
    ...
}
```
