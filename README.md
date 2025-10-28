#include<stdio.h>
int main(){
    int i,n,Day,Month,Year,qty;
    char itemName[30];
    float price,total=0,gst,grandTotal;
    printf("\n                                      MENAKA CLOTHINGS\n\n       ");
    printf("=====================================================================");
    printf("\n\n          Invoice no:58854767                        GSTIN no:AT56956GH\n          ");
    printf("Date(DD/MM/YYYY):");
    scanf("%d/%d/%d",&Day,&Month,&Year);
    printf("\t   --------------------------------------------------------------------");
    printf("\n\tEnter Number of items:");
    scanf("%d",&n);
    printf("\n\n---Enter Item Details---\n");
   for (i = 1; i <= n; i++) {
        printf("\nItem %d name: ", i);
        scanf("%s", itemName);
        printf("Quantity: ");
        scanf("%d", &qty);
        printf("Price per item: ");
        scanf("%f", &price);

        total += qty * price;
    }

    // GST calculation (5%)
    gst = 0.05 * total;
    grandTotal = total + gst;

    printf("\n\n========== BILL SUMMARY ==========\n");
    printf("Total amount (without GST): %f\n", total);
    printf("GST (5%%): %f\n", gst);
    printf("----------------------------------\n");
    printf("Grand Total: %f\n", grandTotal);
    printf("==================================\n");
    printf("Thank you for shopping with us!\n");

    
   return 0;
}
   
