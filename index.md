#include<iostream>
#include<conio.h>
#include<vector>

int main()
{
    int number;
    int list_members;
    int k;
    bool flag = false;
    std::vector <int> list1;
    std::cout << "Enter k: ";
    std::cin >> k;
    std::cout << "Enter Number Of Members: ";
    std::cin >> list_members;

    for(int i = 0; i < list_members; i++){
        std::cout << "Enter list member: ";
        std::cin >> number;
        list1.push_back(number);
        std::cout << std::endl;
    }

    for(int member : list1){
        for(int i = 0; i < list1.size(); i++){
            if(member + list1[i] == k){
                //std::cout << "The Numbers are " << member << " and "<< list1[i] << ".\n" << std::endl;
                flag = true;
                if(flag){
                    std::cout << "True\n\n";
                }
                return 0;
            }
        }
    }
    if(!flag){
        std::cout << "False\n\n";
    }
}

