- 👋 Hi, I’m @Sumangala-S-Sipoy
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Sumangala-S-Sipoy/Sumangala-S-Sipoy is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include<stdio.h>
#include<stdlib.h>
struct distance
{
    int ifeet;
    float finches;
};
struct distance feet(struct distance *d1,struct distance*d2,struct distance *);
int main()
{
    struct distance d1,d2,sum,res;
    printf("enter two values of feet\n");
    scanf("%d%d",&d1.ifeet,&d2.ifeet);
    if(d1.ifeet<0 || d2.ifeet<0)
    {
        printf("Invalid distance input\n");
        exit(0);
    }
    printf("Enter two values of inch\n");
    scanf("%f%f",&d1.finches,&d2.finches);
    if(d1.finches<0 || d2.finches<0)
    {
        printf("Invalid distance input\n");
        exit(0);
    }
    sum=feet(&d1,&d2,&res);
    printf(" %d'feet %.2f'' inch\n",sum.ifeet,sum.finches);
    return 0;
}
struct distance feet(struct distance *d1,struct distance *d2,struct distance *res)
{
   int ft;

   ft=d1->ifeet+d2->ifeet;
   res->finches=d1->finches+d2->finches;

   res->ifeet=res->finches/12;
   res->finches=res->finches-(res->ifeet*12);
   
   res->ifeet=ft+res->ifeet;
   
   printf(" %d' feet %.2f'' inch\n",res->ifeet,res->finches);
   return res;
}
