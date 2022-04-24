# from traceback import print_list


class Node():
    def __init__(self, value):
        self.value = value
        self.next = None

class LinkedList():
    def __init__(self):
        self.head = None
        self.tail = None
        self.length = 0
            
    def append(self, value):
        new_node = Node(value)
        
        if self.length > 0:
            self.tail.next = new_node
            self.tail = new_node
            self.length += 1
        else:
            self.head = new_node
            self.tail = self.head
            self.length = 1
        

    def prepend(self, value):
        new_node = Node(value)
        if self.length > 0:
            new_node.next = self.head
            self.head = new_node
            self.length += 1
        else:
            self.head = new_node
            self.tail = self.head
            self.length += 1

    def printlist(self):
        array = []
        current_node = self.head
        while current_node != None:
            array.append(current_node.value)
            current_node = current_node.next
        return array

    def insert(self,index,value):
        if index >= self.length:
            self.append(value)
        elif index == 0:
            self.prepend(value)
        else:
            # how is this block inserting the value in the list
            # self.head is not being updated.  There is no line that says self.head.next = new_node.
            new_node = Node(value)
            current_node = self.head
            for i in range(index-1):    
                current_node = current_node.next
            new_node.next = current_node.next
            current_node.next = new_node
            self.length += 1



'''past
# class LinkedList():
#     def __init__(self,value):
#         # self.value = value
#         next = None
#         self.head = {'value':value, 'next': next }
#         # self.head = value
#         # self.next = None
#         self.tail = self.head
#         self.length = 1

#
# class LinkedList():
#     def __init__(self,value):
#         self.head = value
#         self.next = None
#         self.tail = self.head
#         self.length = 1
#
#     def append(self, value):
#         # new_node = Node(value)
#         if self.length > 0:
#             self.tail.next = self.tail
#             # self.next = None
#             self.tail = self.value
#             self.length += 1
#         else:
#             self.head = new_node
#             self.tail = self.head
#             self.length = 1
#         return
'''


if __name__ == '__main__':
    a = LinkedList()
    a.append(10)
    a.append(11)
    a.append(12)
    print(a.printlist())
    a.insert(1,10.5)
    print(a.printlist())
    a.prepend(9)
    print(a.printlist())
