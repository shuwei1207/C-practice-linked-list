#include <stdio.h>
#include <stdlib.h>


struct node {       
    int data; 
    struct node *next; 
}; 

typedef struct node node;  

node *createlist(int *arr,int l){
 	int i;
 	node *first,*current,*previous;
	for(i=0;i<l;i++){
		current=(node *) malloc(sizeof(node));
		current->data=arr[i];
		if(i==0){
			first=current;
		 }
		else{
			previous->next=current;	
		}
		current->next=NULL;
		previous=current;
	}
   return first;
}

node *c(node *l1,node*l2){
	int i;
	node *first,*current,*previous,*t;
  	for(i=0,t=l1;t!=NULL;t=t->next,i++){
		current=(node *) malloc(sizeof(node));
		current->data=t->data;
		if(i==0){
			first=current;
		 }
		
		else{
			previous->next=current;
		 }
		current->next=NULL;
		previous=current;
	}
	
	for(t=l2;t!=NULL;t=t->next){
		current=(node *) malloc(sizeof(node));
		current->data=t->data;	
		if(i==0){
			first=current;
		 }
		 
		else{
			previous->next=current;
		 }
		current->next=NULL;
		previous=current;
	}
	return first;
}

node* serch_node(node *first, int target){
	node *node=first;
	while(node!=NULL){
		if(node->data== target) return node;
		else node=node->next;
	 }
	return NULL;
}

node* insert_node(node *l1, node *newNode){
	node *n;
for(n = l1; n != NULL && newNode->next != NULL; newNode = newNode -> next){
	if(n->next->data  >  newNode ->data){
		newNode -> next = n -> next;
		n->next = newNode;
		break;
		}
 }
   return l1;	
}

node* insert_list(node *List,node *newNodeList){
	node *ptr , *insertnode, *NextInsertNode;
	for(insertnode = newNodeList ; insertnode != NULL && NextInsertNode != NULL;insertnode = NextInsertNode){
		for(ptr=List;ptr!=NULL;ptr=ptr->next){
			if(ptr->next->data > insertnode->data){
				NextInsertNode=insertnode->next;
				insertnode->next=ptr->next;
				ptr->next=insertnode;
				break;
			}	
	}
}
    return List;
}

  node *deletenode(node *first,node *deletenode){
	node *ptr = first;
	if(first == NULL){
		printf("沒有東西");
		return NULL;
	 }
	
	if(first == deletenode){
		first = first->next;
	 }
	 
	else{
		while(ptr->next != deletenode) ptr=ptr->next;
		ptr->next=deletenode->next;
	 } 
	free(deletenode);
	return first;
}

int main() {
	int arr1[]={1,3,9};
	int arr2[]={2,5,7};
	node *list1,*list2,*list3,*list4,*list5,*list6,*t,*t1,*t2;
	
	list1=createlist(arr1,3);
	list2=createlist(arr2,3);
	list3=c(list1,list2);
	list5=insert_list(list1,list2);

	int i;
	printf("開始節點  ");	
	for(t=list5,i=1;t!=NULL;printf("->第%d個節點 DATA=%d ",i,t->data),i++,t=t->next);

	return 0;
	}
