#include <iostream>
using namespace std;
class shape{
    protected:
    int width, height;
    
    public:
    shape(int x=0,int y=0){
        width=x;
        height=y;
    }
    int area(){
        cout<<"enter parent class area"<<endl;
        return 0;
    }
};
    class rectangle:public shape{
        public:
        rectangle(int x=0,int y=0):shape(x,y){}
        
        int area(){
            cout<<"enter rectangle class area"<<endl;
            return (width*height);
    }
};
    class triangle:public shape{
        public:
        triangle(int x=0,int y=0):shape(x,y){}
        
        int area(){
            cout<<"enter triangle class area"<<endl;
            return (2/width*height);
    }
};
int main(){
    shape *shape;
    rectangle rec(10,7);
    triangle tri(10,5);
    
    shape=&rec;
    shape->area();
    shape=&tri;
    shape->area();
    return 0;
    
}
    
