# LinkedList

```javascript

//Insert at "last" and "first" in linked list (  O(1) ) by using tail.

     
    class Node{
        constructor(data){
         this.data=data;
         this.next=null;
        }
    }
    class LinkedList{
        constructor(data,location){
        this.head=null;
        this.tail=null;
        }

        addNode(dataI,locationI){
            let node=new Node(dataI);
       if(this.head==null){
        this.head=node;
        this.tail=node;
       }else{
        if(locationI=="first"){
          node.next=this.head;
          this.head=node;
        }else if(locationI=="last"){
            node.next=null;
            this.tail.next=node;
            this.tail=node;
        }
       }
        }
    }

    let linkedList=new LinkedList();
    linkedList.addNode(33,"first");
    linkedList.addNode(40,"first"); 
    linkedList.addNode(55,"first");
    linkedList.addNode(500000,"last");
    console.log(linkedList)

```

<img src="../insert.png" />

