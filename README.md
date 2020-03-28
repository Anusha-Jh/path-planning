# path-planning
class node:
         def __init__(self,data):
                  self.data=data
                  self.next=None
class LinkedList: 
  
    def __init__(self): 
        self.start = None

          def  insert(self,n_node,n_data):
# if no node is present
                   if self.start is None: 
            n_node.next = self.start
            n_node = node(n_data)
            self.start = n_node 

# if only one node is present
        elif self.start.data >= n_node.data: 
            n_node.next = self.start 
            self.start = n_node
            n_node = node(n_data) 
# for more than one node present
# s is the current node 
        else:
 
            s = self.head 
            while(s.next is not None and s.next.data <  n_node.data): 
                s = s.next
              
            n_node.next = s.next
            s.next = n_node 
            n_node = node(n_data)

    def print(self): 
        p = self.start 
        while(p!=None): 
            print p.data, 
            p= p.next


l_list = LinkedList() 
n_node = node(1) 
l_list.insert(n_node) 
n_node = node(4) 
l_list.insert(n_node) 
n_node = node(3) 
l_list.insert(n_node) 
n_node = node(2) 
l_list.insert(n_node) 
n_node = node(6) 
l_list.insert(n_node) 
n_node = node(5) 
l_list.insert(n_node) 
print "Sorted Linked List:"
l_list.print()

