Returns a new list without any consecutively repeating elements. Equality is
determined by applying the supplied predicate to each pair of consecutive elements. The
first element in a series of equal elements will be preserved.

Acts as a transducer if a transformer is given in list position.

@func
@memberOf R
@since v0.14.0
@category List
@sig (a, a -> Boolean) -> [a] -> [a]
@param {Function} pred A predicate used to test whether two items are equal.
@param {Array} list The array to consider.
@return {Array} `list` without repeating elements.
@see R.transduce
@example

     var l = [1, -1, 1, 3, 4, -4, -4, -5, 5, 3, 3];
     R.dropRepeatsWith(R.eqBy(Math.abs), l); //=> [1, 3, 4, -5, 3]
