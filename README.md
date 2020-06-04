# insertion-sort
using System;
using System.Collections.Generic;
namespace GrowingWithTheWeb.Sorting
public void Sort(IList<T> list)
    {
        for (int i = 1; i < list.Count; i++) {
            T item = list[i];
            int indexHole = i;
            while (indexHole > 0 && list[indexHole - 1].CompareTo(item) > 0) {
                list[indexHole] = list[--indexHole];
            }
            list[indexHole] = item;
        }
    }
}
public class InsertionSort {
    public static <T extends Comparable<T>> void sort(T[] array) {
        for (int i = 1; i < array.length; i++) {
            T item = array[i];
            int indexHole = i;
            while (indexHole > 0 && array[indexHole - 1].compareTo(item) > 0) {
                array[indexHole] = array[--indexHole];
            }
            array[indexHole] = item;
 */
function sort(array, compare) {
  for (var i = 1; i < array.length; i++) {
    var item = array[i];
    var indexHole = i;
    while (indexHole > 0 && compare(array[indexHole - 1], item) > 0) {
      array[indexHole] = array[--indexHole];
    }
    array[indexHole] = item;
    if (sortExternal.shiftObserver) {
      sortExternal.shiftObserver(i, indexHole);
    }
  }

  return array;
}
def default_compare(a, b):
  if a < b:
    return -1
  elif a > b:
    return 1
  return 0

def sort(array, compare=default_compare):
  for i in range(1, len(array)):
    item = array[i]
    indexHole = i
    while indexHole > 0 and compare(array[indexHole - 1], item) > 0:
      array[indexHole] = array[indexHole - 1]
      indexHole -= 1
    array[indexHole] = item
  return array
module InsertionSort
  # Sorts an array using insertion sort.
  def self.sort(array, compare = lambda { |a, b| a <=> b })
    (1..array.length - 1).each do |i|
      item = array[i]
      indexHole = i
      while indexHole > 0 and compare.call(array[indexHole - 1], item) > 0
        array[indexHole] = array[indexHole - 1]
        indexHole = indexHole - 1
      end
      array[indexHole] = item
    end
  end
end
