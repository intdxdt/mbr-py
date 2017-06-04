# minimum bounding box - python
Minimum bounding box operations in python

# example
```py
box1 = MBR(0, 0, 0, 0)
box1.expand_include_xy(2, 2)
print box1  # POLYGON ((0 0, 0 2, 2 2, 2 0, 0 0))

box2 = MBR(0, 0, 2, 2)
print box2.equals(box1) # True
print box1.height       # 2
print box1.width        # 2
print box1.area         # 4
print box1.center       # (1.0, 1.0)

#let p = point(1.7, 1.5)
p = 1.7, 1.5
print box2.intersects_point(p) #True

box3 = MBR(1.7, 1.5, 3.0, 1.9)
box4 = MBR(2.5, 3, 4.0, 5.0)

#intersects & intersection 
print box2.intersects(box3) # True
iters, bln = box2.intersection(box3)
# mbr, intersects
# MBR (1.7, 1.5, 2.0, 1.9), True

print box2.intersects(box4) # False
inter, bln = box2.intersection(box4)
# MBR(nan, nan, nan, nan), False

print box1.distance(box4) #1.118



```
## methods 
    as_poly_array
    is_point
    clone
    as_tuple
    equals
    translate
    intersection
    intersects_bounds
    contains
    contains_xy
    completely_contains_xy
    completely_contains_mbr
    disjoint
    intersects
    intersects_point
    expand_include_mbr
    expand_by_delta
    expand_include_xy
    distance
    distance_square


## properties
    llur
    width
    height
    area
    center

# lic
MIT