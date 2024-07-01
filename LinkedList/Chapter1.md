# LinkedList

```javascript
 class Node {
        constructor(data) {
          this.data = data;
          this.next = null;
        }
      }

      class LinkedList {
        constructor() {
          this.head = null;
          this.tail = null;
        }
        create(arr) {
          this.head = new Node(arr[0]);
          this.tail = this.head;

          for (let i = 1; i < arr.length; i++) {
            let node = new Node(arr[i]);
            this.tail.next = node;
            this.tail = node;
          }
        }
        display() {
          let p = this.head;
          while (p) {
            console.log(p.data);
            p = p.next;
          }
        }
        reverse(p = this.head) {
          if (p) {
            this.reverse(p.next);
            console.log(p.data);
          }
        }
        rdisplay(p = this.head) {
          if (p) {
            console.log(p.data);
            this.rdisplay(p.next);
          }
        }

        // Length of linked list from 1 to n
        length() {
          let p = this.head;
          let sum = 0;
          while (p) {
            sum++;
            p = p.next;
          }
          return sum;
        }
        rlength(p = this.head) {
          if (p == null) {
            return 0;
          } else {
            // return this.rlength(p.next) + 1;
            return 1 + this.rlength(p.next);
          }
        }

        sum() {
          let p = this.head;
          let sum = 0;
          while (p) {
            sum += p.data;
            p = p.next;
          }
          return sum;
        }

        rsum(p = this.head) {
          if (p == null) {
            return 0;
          } else {
            // return p.data + this.rsum(p.next);
            return this.rsum(p.next) + p.data;
          }
        }
        // with third variable sum
        rrsum(p = this.head, sum = 0) {
          if (p == null) {
            return sum;
          } else {
            // return p.data + this.rsum(p.next);
            return this.rrsum(p.next, sum + p.data);
          }
        }

        // max element in the list
        max() {
          let p = this.head;
          let max = Number.NEGATIVE_INFINITY;
          while (p) {
            if (max < p.data) {
              max = p.data;
            }
            p = p.next;
          }
          return max;
        }
        rmax(p = this.head, max = Number.NEGATIVE_INFINITY) {
          if (p == null) {
            return max;
          }
          if (p.data > max) {
            max = p.data;
          }
          return this.rmax(p.next, max);
        }
        armax(p = this.head) {
          if (!p) {
            return Number.NEGATIVE_INFINITY; // Base case: reached the end of the list
          }
          const x = this.armax(p.next);
          return x > p.data ? x : p.data;
        }
        armin(p = this.head) {
          if (!p) {
            return Number.POSITIVE_INFINITY; // Base case: reached the end of the list
          }
          const x = this.armin(p.next);
          return Math.min(x, p.data); // Compare x with current node's data
        }

        linearSearch(key) {
          let p = this.head;
          while (p) {
            if (p.data == key) {
              return p;
            }
            p = p.next;
          }
          return null;
        }
        rlinearSearch(key, p = this.head) {
          if (p == null) {
            return null;
          }
          if (key === p.data) {
            return p;
          }
          return this.rlinearSearch(key, p.next);
        }
      }

      let list = new LinkedList();
      //       console.log(list);
      list.create([100, 20, 30000, 400, 5500, 6000, 700, 800, 900, 1000]);
      // console.log(list);
      // list.display();
      // list.rdisplay();
      // list.reverse();
      // console.log(list.length());
      // console.log(list.rlength());
      // console.log(list.sum());
      // console.log(list.rrsum());
      // console.log(list.rsum());
      // console.log(list.max());
      // console.log(list.rmax());
      // console.log(list.armin());
      // console.log(list.linearSearch(1000));
      console.log(list.rlinearSearch(100));

```

<img src="../insert.png" />

