# trainLinkList-

## Problem Domain

You have a train. You have to add up all the passengers on the train, but you do not know how long the train is.

## EXAMPLE DATA

You start at the front of the train.

## Visual

## Train

```mermaid
graph LR
head --> A(Node A)-->|link| B(Node B)
B--> |link| C[null]
```

```mermaid
graph LR
 start --> A(info)--> |link| B(info)
B--> |link| C[null]
```

## Node A

- count Passengers say there is 20
- need to store 20
- newData = 20
- check if there is next
- if there is a next then move to next
- there is a next

```mermaid
graph LR
 start --> A(20)--> |link| B(info)
B--> |link| C[null]
```

## Node B

- count Passengers say there is 10
- need to store 10
- new data = 10
- then need to add the data
- Then store new total into storeTotalCount
- check if there is next
- if there is a next then move to next else if there is no next then return storeTotalCount

```mermaid
graph LR
 start --> A(20)--> |link| B(10)
B--> |link| C[null]
```

## Algorithm

1. You start at front of the Train (Head)
2. You count all the passengers on the train and store total count.
3. Then go to the door (link) check if door is unlocked if unlocked then go through (next).
4. Count all passengers on train and store in new store total and add store total.
5. Then go to the door (link) check if door is unlocked. If door is not unlocked. Then your at the end of train.
6. Then return store total amount of passengers on train.

## Pseudocode

- node of the Linked List
- create node
- function to insert a node at the beginning
- function push (head, newData) {
  - assign node
  - let newNode = to new Node();
    - put in the data
    - newNode.data = newData;
    - where you link the old list of node to new node
    - newNode.next = head;
    - move the head to point to the new nodes
    - head = newNode;
    - return head;
}

- function to recursively find the sum of
- nodes of the given linked list
  - function sumOfNodes(head) {

    - if head equal null
      - if (head == null)
      - return;

    - recursively traverse the remaining nodes
    - sumOfNodes(head.next);

    - acquire the sum
    - sum = sum + head.data;

  }

## Code

## Big O

Time: O(n)
Space: O(n)