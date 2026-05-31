class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
        
node1 = Node('Buksan mo by Willie Revillame')
head = node1

def insertNodeAtTheBeginning(data):
    global head
    newNode = Node(data)
    
    if(head == None):
        head = newNode
    else:
        newNode.next = head
        head = newNode
        

def traverseLinkedList():
    current = head
    while(current):
        print(current.data, end=" -> ")
        current = current.next
        
        
def insertNodeAtEnd(data):
    newNode = Node(data)
    global head
    
    if(head == None):
        head = newNode
    else:
        current = head
        while(current.next != None):
            current = current.next
        current.next = newNode
        

def insertNodeAfterGivenNode(data, node):
    newNode = Node(data)
    global head
    if(head == None):
        head = newNode
    else:
        current = head
        prev = head
        
        while(prev.data != node):
            prev = current
            current = current.next
            
            if(current == None):
                print('The node does not exist')
                return
            
    newNode.next = current
    prev.next = newNode
            
insertNodeAtTheBeginning('kabisado iv of spades')
insertNodeAtTheBeginning('tahanan- El Manu')
insertNodeAtTheBeginning('Ripples - beabadoobee')
insertNodeAtTheBeginning('Naiilang-Le John')
insertNodeAtEnd('Nangangamba- Zack Tabudlo')
insertNodeAtEnd('Tumalon- Solace Out The Door')
insertNodeAtEnd('Tayo- Le John')
insertNodeAfterGivenNode('Tahanan- El Manu, Ripples-beabadoobee, Naiilang- Le John, Nangangamba-Zack Tabudlo, Tumalon- Salace Out The Door, Tayo- Le John')

traverseLinkedList()
