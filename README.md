#include <stdio.h>
#include <stdlib.h>
struct Info { //отдельная структура для сбора нужной информации
    struct Elem ** p_field; //указатель на поле внутри родительской структуры, хранящее указатель на удаляемый элемент
    struct Elem * del_el;//удаляемый элемент
    struct Elem * most_right;//максимальный эл-т левого поддерева
    struct Elem * parent_most_right;
}
struct Elem {
	int val; // значение, которое хранится в элементе ((!) может быть указателем на строку, например)
	struct Elem * lv, * pr; // указатели на левого и правого потомков
};
int main{

}
void del_elem(struct Info * del_el) { //функция удаления элемента (подаем в функцию значение удаляемого эл-та)
if ((del_el -> lv) == NULL) {//нет левого потомка удаляемого эл-та

    if ((del_el -> pr) == NULL) { //если и правого потомка нет
       
        del_el -> val == NULL;
        * p_field == NULL;//?? так ли мы обNULLяем то, что в род эл-те про уд эл-т 

    }
    else{ //нет левого, но есть правый потомок
        * p_field == del_el -> pr;           
    }    
}
else{
    if (find_parent(most_right) == )
}   

}

struct Elem * find_most_right (x){//рассматриваем левое поддерево удаляемого элемента

    struct Elem * p == x -> lv; // p - указатель на текущий элемент на каждой итерации
    while(1){
        if (p -> pr != NULL){
            p = p -> pr;
        }
        else{
            most_right == p;
            return p;
        }
    }
}

struct Elem * find_parent (int x){ 

    struct Elem * p == root; //p - указатель на текущий элемент на каждой итерации
    if (x == p){ 
     return NULL;
    }
    if (p -> lv == NULL) && (p -> pr == NULL){
        return NULL;
    }
    else{
        while (1){
            if (p -> pr == x) || (p -> lv == x){
                return p;
            }
            else{
                if (x > p -> val){
                    if (p -> pr != NULL){
                        p = p -> pr;
                    }
                    else{
                        return NULL;
                    }
                else{
                    if (p -> lv != NULL){
                        p = p -> lv;
                    }
                    else{
                        return NULL;
                    }
                }
                }
            }
        }   
    }
} 
