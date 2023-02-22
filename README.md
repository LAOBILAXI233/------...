
简单的猜数字小游戏，…


#include<iostream>
using namespace std;
#include<ctime>
int main()
{
    srand((unsigned int)time(NULL));
   int num = rand() % 100 + 1;
    int a = 0;
    cout << "请输入0-100的数字" << endl;
    int change = 0;
    
        while (1)
        {
            cin >> a;
            if (a > 0 && a < 101)
            {
                change++;
                cout << "你还有" << 5 - change << "次机会" << endl;
                if (change < 5)
                {
                  
                    if (a > num)
                    {
                        cout << "big " << endl;
                    }
                    else if (a < num)
                    {
                        cout << "太小了" << endl;
                    }
                    else
                    {
                        cout << "太大了" << endl;
                        break;
                    }
                }
                else
                {
                    cout << "no change " << endl;
                    cout << "正确答案" << num << endl;
                    break;
                }
            }
            else
            {
                cout << "你输入nm呢" << endl;
                break;
            
            }
        }
  
        
    
    system("pause");

    return 0;


    }
