# bank-management-system01
DIU Project
#include<stdio.h>
#include<stdlib.h>
//father's name=fname
char name[30],fname[30],address[30],mobile_number[15],ac_no[10];
//DOB month=dm DOB day=dd DOB year=dy
//request money
int age,dd,dm,dy,req_money;
long int nid;
void mmenu();
void na();
void sp();
void ea();
void ds();
void ls();
void fordelay(int j)
{
    int i,k;
    for(i=0; i<j; i++)
        k=i;
}
int main()
{
home:
    system("cls");
    char pass[10],password[10]="123";
    int i;
    printf("\n\n\n");
    printf("\n\t\t\t\t            ---------***---------");
    printf("\n\t\t\t            ~~~~~~~~~~~~~~~~~ * ~~~~~~~~~~~~~~~~~ ");
    printf("\n\t\t\t        |                                           |");
    printf("\n\t\t\t        |                  WELCOME                  |");
    printf("\n\t\t\t        |                    TO                     |");
    printf("\n\t\t\t        |                  \"DIUCB\"                  |");
    printf("\n\t\t\t        |      DAFFODIL INTERNATIONAL UNIVERSITY    |");
    printf("\n\t\t\t        |               CENTRAL BANK                |");
    printf("\n\t\t\t        |                                           |");
    printf("\n\t\t\t            ~~~~~~~~~~~~~~~~~ * ~~~~~~~~~~~~~~~~~ ");
    printf("\n\t\t\t\t            ---------***---------");
    printf("\n\n\t\t\t\tEnter the admin password to login: ");
    scanf("%s",pass);
    if (strcmp(pass,password)==0)
    {
        printf("\n\t\t\t\tPassword Match! LOADING.....");
        fordelay(1000000000);
        mmenu();

    }
    else
    {
        printf("\n\t\t\t\tInvalid Password.");
        fordelay(1000000000);
        goto home;
    }
    getch();

}
void mmenu()
{
    int choice;
    //main menu choice
mmc:

    system("cls");
    system("color 9");
    printf("\n\n\n\t\t\t\xB2\xB2\xB2\xB2\xB2\xB2\xB2 WELCOME TO THE MAIN MENU \xB2\xB2\xB2\xB2\xB2\xB2\xB2");
    printf("\n\n\t\t1.Create new account\n\t\t2.Different schemes\n\t\t3.Loan system\n\t\t4.Update informationt\n\t\t5.Removing existing account\n\t\t6.Show customers profile\n\t\t7.Calculate after transaction\n\t\t8.Customer of the year\n\t\t9.Show the list of existing account\n\t\t10.Exit\n\n\n\n\n\t\tEnter your choice: ");
    scanf("%d",&choice);
    system("cls");
    switch(choice)
    {
    case 1:
        //new account
        na();
        goto mmc;
    case 2:
        //different schemes
        ds();
        goto mmc;

    case 3:
        //loan system
        ls();
        goto mmc;
        break;
    /* case 4:
     //update information
         ui();
         goto mmc;
         break;
     case 5:
     //removing account
         ra();
         goto mmc;
         break;*/
    case 6:
        //show profile
        sp();
        goto mmc;
    /* case 7:
         at();
         goto mmc;
         break;
     case 8:
         cy();
         goto mmc;
         break;*/
    case 9:
        //existing account
        ea();
        goto mmc;
    case 10:
        printf("\n\n\n\n\n\n\n\n\n\n\n\n\n\t\t\t\t\t\tThank You For Visit...");
        fordelay(1000000000);
        main();
        break;
    default:
        printf("\n\n\n\n\n\n\n\n\n\n\n\n\n\t\t\t\tInvalid selection. Please choose a valid number...");
        fordelay(10000000000);
        goto mmc;

    }

}
void na()
{
    system("cls");
    fflush(stdin);
    printf("\n\n\n\t\t\t\xB2\xB2\xB2\xB2\xB2\xB2\xB2 WELCOME TO NEW ACCOUNT FORM \xB2\xB2\xB2\xB2\xB2\xB2\xB2");
    printf("\n\t\tACC NO: ");
    gets(ac_no);
    printf("\n\t\tEnter Name: ");
    gets(name);
    printf("\n\t\tEnter Father Name: ");
    gets(fname);
    printf("\n\t\tDate of Birth: ");
    scanf("%d/%d/%d",&dd,&dm,&dy);
    printf("\n\t\tEnter Age: ");
    scanf("%d",&age);
    fflush(stdin);
    printf("\n\t\tEnter Address: ");
    gets(address);
    printf("\n\t\tEnter Mobile Number: ");
    gets(mobile_number);
    printf("\n\t\tEnter NID Number: ");
    scanf("%ld",&nid);
    printf("\n\t\tFirst deposit money: ");
    scanf("%d",&req_money);
    printf("\n\t\tAccount Created Successfully...");
    fordelay(1000000000);
}
void sp()
{
    system("cls");
    fflush(stdin);
    //check account number
    char check_accno[10];
    printf("\n\n\n\t\t\t\xB2\xB2\xB2\xB2\xB2\xB2\xB2 Show Profile \xB2\xB2\xB2\xB2\xB2\xB2\xB2");
    printf("\n\t\tEnter the account number: ");
    gets(check_accno);
    if(strcmp(check_accno,ac_no)==0)
    {
        int money;
        money=req_money;
        printf("\n\t\tAccount NO: %s",ac_no);
        printf("\n\t\tName: %s",name);
        printf("\n\t\tFather's Name: %s",fname);
        printf("\n\t\tDate of Birth: %d/%d/%d",dd,dm,dy);
        printf("\n\t\tAge: %d",age);
        printf("\n\t\tAddress: %s",address);
        printf("\n\t\tMobile Number: %s",mobile_number);
        printf("\n\t\tNID Number: %ld",nid);
        printf("\n\t\tBalance: %d",money);
    }
    else printf("\n\t\tInvalid Account");
    fordelay(100000000);
    getch();
}
void ea()
{
    int money=req_money;
    system("cls");
    printf("\n\n\n\t\t\t\xB2\xB2\xB2\xB2\xB2\xB2\xB2 Existing Account \xB2\xB2\xB2\xB2\xB2\xB2\xB2");
    printf("\n\t\t1.");
    printf("\n\t\tAccount NO: 03112022");
    printf("\n\t\tName: Arpon");
    printf("\n\t\tFather's Name: Newaj");
    printf("\n\t\tDate of Birth: 12/12/2001");
    printf("\n\t\tAge: 20");
    printf("\n\t\tAddress: Gazipur");
    printf("\n\t\tMobile Number: 017000000");
    printf("\n\t\tNID Number: 9191919191");
    printf("\n\t\tBalance: 1000");
    printf("\n\t\t2.");
    printf("\n\t\tAccount NO: %s",ac_no);
    printf("\n\t\tName: %s",name);
    printf("\n\t\tFather's Name: %s",fname);
    printf("\n\t\tDate of Birth: %d/%d/%d",dd,dm,dy);
    printf("\n\t\tAge: %d",age);
    printf("\n\t\tAddress: %s",address);
    printf("\n\t\tMobile Number: %s",mobile_number);
    printf("\n\t\tNID Number: %ld",nid);
    printf("\n\t\tBalance: %d",money);
    getch();
}
void ds()
{
dschoice:
    system("cls");
    int choice;
    printf("\n\n\n\t\t\t\xB2\xB2\xB2\xB2\xB2\xB2\xB2 Different Schemes \xB2\xB2\xB2\xB2\xB2\xB2\xB2");
    printf("\n\t\t1.Fixed Deposite");
    printf("\n\t\t2.Monthly Profit Scheme");
    printf("\n\t\t3.Quarterly Profit Scheme");
    printf("\n\t\t4.Double Profit Scheme");
    printf("\n\t\t5.Millionier Scheme");
    printf("\n\t\t0.Main Menu");
    printf("\n\t\tChoose an option for details of the scheme: ");
    scanf("%d",&choice);
    printf("\n\t\tInstallment Type\t\tInstallment Amount\t\tInterest Rate\t\t\t\tPeriod\t\t\t\tPayable After Maturity");
    if(choice==1)
    {
        printf("\n\n\t\tOne-Time Installment\t\t\t\t\t\t6.00%%\t\t\t\t01 year but less than 03 years\t\t\t\t");
    }
    else if(choice==2)
    {
        printf("\n\n\t\tOne-Time Installment\t\t1,00,000/-\t\t\t7.00%%\t\t\t\t\t07 years \t\t\tMonthly Profit 583/-");
    }
    else if(choice==3)
    {
        printf("\n\n\t\tOne-Time Installment\t\t1,00,000/-\t\t\t6.50%%\t\t\t\t\t03 years \t\t\tQuarterly Profit 1,625/-");
    }
    else if(choice==4)
    {
        printf("\n\n\t\tOne-Time Installment\t\t10,000/-\t\t\t7.00%%\t\t\t\t\t12 years \t\t\t");
    }
    else if(choice==5)
    {
        printf("\n\n\t\tMonthly-Time Installment\t14,600/-\t\t\t6.25%%\t\t\t\t\t05 years \t\t\t\t10,00,000/-");
    }
    else if(choice==0)
    {
        mmenu();
    }
    else
    {
        printf("\n\n\n\n\n\n\n\n\n\n\n\n\n\t\t\t\tInvalid selection. Please choose a valid number...");
    }
    getch();
    goto dschoice;
}
void ls()
{
lschoice:
    system("cls");
    int choice,amount;
    printf("\n\n\n\t\t\t\xB2\xB2\xB2\xB2\xB2\xB2\xB2 Loan System \xB2\xB2\xB2\xB2\xB2\xB2\xB2");
    printf("\n\n\t\t1.3years Loan(Maximum 2,00,000 with 4%%  interest)");
    printf("\n\n\t\t2.5years Loan(Maximum 5,00,000 with 5%%  interest)");
    printf("\n\n\t\t3.10years Loan(Maximum 10,00,000 with 6%%  interest)");
    printf("\n\n\t\t0.Main Menu");
    printf("\n\n\t\tEnter your choice: ");
    scanf("%d",&choice);
    if(choice==1)
    {
        printf("\n\t\tEnter the amount: ");
        scanf("%d",&amount);
        printf("\n\t\tLoan amount: %d",amount);
        printf("\n\t\tPeriod: 3years");
        printf("\n\t\tTotal Interest: %.2f",(amount*.04));
        printf("\n\t\tTotal Payable Amount: %.2f",(amount+(amount*.04)));
    }
    else if(choice==2)
    {
        printf("\n\t\tEnter the amount: ");
        scanf("%d",&amount);
        printf("\n\t\tLoan amount: %d",amount);
        printf("\n\t\tPeriod: 5years");
        printf("\n\t\tTotal Interest: %.2f",(amount*.05));
        printf("\n\t\tTotal Payable Amount: %.2f",(amount+(amount*.05)));
    }
    else if(choice==3)
    {
        printf("\n\t\tEnter the amount: ");
        scanf("%d",&amount);
        printf("\n\t\tLoan amount: %d",amount);
        printf("\n\t\tPeriod: 10years");
        printf("\n\t\tTotal Interest: %.2f",(amount*.06));
        printf("\n\t\tTotal Payable Amount: %.2f",(amount+(amount*.06)));
    }
    else if(choice==0)
        mmenu();
    else
    {
        printf("\n\n\n\n\n\n\n\n\n\n\n\n\n\t\t\t\tInvalid selection. Please choose a valid number...");
    }
    getch();
    goto lschoice;
}
