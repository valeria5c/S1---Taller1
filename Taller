#include <stdio.h>

int main ()
{
    int ID, stock=0, menu, vent_unid, stock_nuevo, total_unidades_vendidas = 0;
    float pre_unit=0, ganancias = 0, descuento, precio_final, venta_total;
    char nombre[50];

    printf("\n Registrar los datos del producto \n");
    printf("Ingrese el nombre del producto: \n");
            getchar();
            scanf(" %[^\n]", nombre);
            printf("Ingrese el ID del producto: \n");
            scanf("%d", &ID);
            do
            {
                printf("Ingrese el stock del producto: \n");
                scanf("%d", &stock);
                if (stock < 0)
                {
                    printf("Cantidad invalida.\n");
                }
            } while (stock < 0);
            
            do
            {
                printf("Ingrese el precio unitario del producto: \n");
                scanf("%f", &pre_unit);
                if (pre_unit < 0)
                {
                    printf("Cantidad invalida.\n");
                }
            } while (pre_unit < 0);

            printf("Producto ingresado con éxito \n");
    
    do
    {
        printf("\nMENU \n");
        printf("1. Vender unidades del producto: \n");
        printf("2. Reabastecer el producto: \n");
        printf("3. Consultar información actualizada del producto: \n");
        printf("4. Ganancias obtenidas hasta el momento : \n");
        printf("5. Salir del programa: \n");
        printf("Ingrese la opción que desea realizar: \n");
        scanf("%d", &menu);
    
        switch (menu)
        {

        case 1:
        
            do
            {
                printf("Ingrese las unidades que desea vender del producto: \n");
                scanf("%d", &vent_unid);
            } while (vent_unid<1);
        
            if (stock<vent_unid)
            {
                printf("El stock es insuficiente para realizar la venta \n");
            } else {
                do
                {
                    printf("Ingrese el porcentaje de descuento: ");
                    scanf("%f", &descuento);
                    if (descuento < 0 || descuento > 100) {
                    printf("Descuento invalido\n");
                    }
                } while (descuento < 0 || descuento > 100);
                
                precio_final = pre_unit * (1 - descuento / 100);
                venta_total = precio_final * vent_unid;
                printf("Venta Realizada con éxito \n");
                printf("Precio final por unidad: %.2f\n", precio_final);
                printf("Total de esta venta: %.2f\n", venta_total);

                stock -= vent_unid;
                total_unidades_vendidas += vent_unid;
                ganancias += venta_total;

            }

            break;
    
        case 2:
            printf("\nStock actual: %d\n", stock);
            
            do
            {
                printf("Ingrese la cantidad que desea agregar al stock: ");
                scanf("%d", &stock_nuevo);
                if (stock_nuevo < 0)
                {
                    printf("Cantidad invalida.\n");
                }
                
            } while (stock_nuevo < 0);
            
            if (stock_nuevo > 0) {
                stock += stock_nuevo;
                printf("Stock actualizado: %d\n", stock);
            }
            break;

        case 3:
            printf("\n Informacion del producto \n");
            printf("ID: %d\n", ID);
            printf("Nombre: %s\n", nombre);
            printf("Stock: %d\n", stock);
            printf("Precio unitario: %.2f\n", pre_unit);
            printf("Unidades vendidas: %d\n", total_unidades_vendidas);
            break;

        case 4:
            printf("\nGanancias obtenidas: %.2f\n", ganancias);
            break;

        case 5:
            printf("\nGracias por usar el programa\n");
            break;
    
        default:
            printf("\nOpcion invalida\n");
        }
    } while (menu!=5);

    return 0;
   
}
