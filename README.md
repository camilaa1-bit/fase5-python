# fase5-python
Estudiante: camila andrea castro Noa
# =====================================
# PROBLEMA 3 - CONTROL DE INVENTARIO
# =====================================

# Matriz de artículos
inventario = [
    ["A101", "Teclado", 5, 10],
    ["A102", "Mouse", 15, 10],
    ["A103", "Monitor", 3, 8],
    ["A104", "USB", 20, 15],
    ["A105", "Impresora", 2, 5]
]

# Función para calcular cuánto pedir
def calcular_pedido(stock_actual, stock_minimo):

    if stock_actual < stock_minimo:
        return stock_minimo - stock_actual
    else:
        return 0


# Título
print("===== LISTA DE PEDIDOS =====")


# Recorrer la matriz
for articulo in inventario:

    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    cantidad_pedir = calcular_pedido(stock_actual, stock_minimo)

    print("Artículo:", nombre)
    print("Código:", codigo)
    print("Cantidad a pedir:", cantidad_pedir)
    print("--------------------------")


# Pausa para cerrar el programa
input("Presione ENTER para salir...")
