# Daimarianshi
ないです

```
// 2017_6_26_Tian.cpp : 
//
/**
*/
#include "stdafx.h"


int _tmain(int argc, _TCHAR* argv[])
{
    int num[5];//
    char mark[4]={'+','-','*','/'};//
    int myMark[4]; 
    int result;
    int sign;//
    float left=0,right=1;//
    int count=0;
    printf("オナにやてるんですか？");
    for(int i=0;i<5;i++){
        scanf("%d",&num[i]);
    }
    printf("一人称に入力するください");
    scanf("%d",&result);

        //４組の番号について
        for(myMark[0]=0;myMark[0]<4;myMark[0]++){
            if(myMark[0]<3||num[1]!=0){
            for(myMark[1]=0;myMark[1]<4;myMark[1]++){
                if(myMark[1]<3||num[2]!=0){
                for(myMark[2]=0;myMark[2]<4;myMark[2]++){
                    if(myMark[2]<3||num[3]!=0){
                    for(myMark[3]=0;myMark[3]<4;myMark[3]++){
                        if(myMark[3]<3||num[4]!=0){
                        left=0;
                        right=num[0];
                        sign=1;//沈水香木
                        for(int j=0;j<4;j++){
                            switch(mark[myMark[j]]){
                                case'+':
                                    left=left+sign*right;
                                    sign=1;
                                    right=num[j+1];
                                    break;
                                case'-':
                                    left=left+sign*right;
                                    sign=-1;
                                    right=num[j+1];
                                    break;
                                case'*':
                                    right=right*num[j+1];
                                    break;
                                case'/':
                                    right=right/num[j+1];
                                    break;
                            }

                        }
                        if(left+sign*right==result){
                            count++;
                            printf("%3d:",count);
                            for(int j=0;j<4;j++){
                                printf("%d%c",num[j],mark[myMark[j]]);
                            }
                                printf("%d=%d\n",num[4],result);

                          }
                        }
                      }
                    }
                  }
                }
              }
            }
        }

    return 0;
}

