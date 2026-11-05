class Producto:
    def __init__(self, nombre, tipo, precio, stock):
        self.nombre = nombre
        self.tipo = tipo
        self.precio = precio
        self.__stock = 0
        self.set_stock(stock)
    
    def get_stock(self):
        return self.__stock
 
    def set_stock(self, nuevo_stock):
        if nuevo_stock >= 0:
            self.__stock = nuevo_stock
        else:
            print("Stock inválido")
 
    def mostrar_datos(self):
        print("Nombre:",self.nombre,"\nTipo:",self.tipo,"\nPrecio:",self.precio,"\nStock:",self.__stock,"\n ")
  
    def vender(self, cantidad):
        if cantidad <= 0:
            print("Cantidad invalida")
        elif cantidad <= self.__stock:
            self.__stock -= cantidad
            print("Venta realizada")
            print("Stock restante:",self.__stock)
        else:
            print("Stock insuficiente")
        print(" ")
    
    def reponer(self, cantidad):
         if cantidad > 0:
             self.__stock = self.__stock + cantidad
             print("Reposición realizada")
         else:
            print("Cantidad inválida")

class Alimento(Producto):
    def __init__(self, nombre, precio, stock, vencimiento):
       super().__init__(nombre, "Alimento", precio, stock)
       self.vencimiento = vencimiento
    
    def mostrar_vencimiento(self):
        print("Vto:",self.vencimiento)

class Electronico(Producto):
    def __init__(self, nombre, precio, stock, garantia):
        super().__init__(nombre,"Electronico",precio,stock)
        self.garantia_meses = garantia
    
    def mostrar_garantia(self):
        print("Garantia:", self.garantia_meses ,"meses")

#Actividad 1
producto = Producto("Arroz","Alimento",2000,8)

producto.vender(3)
print(producto.get_stock())
# pienso que va a quedar 5
producto.vender(10)
print(producto.get_stock())
#no se va a poder vender
producto.set_stock(-5)
print(producto.get_stock())
#no va a funcionar

#Actividad 2
producto.reponer(5)
print(producto.get_stock())

producto.reponer(-2)
print(producto.get_stock())
#la segunda instruccion no deberia afectar porque hay un if que valida si es mayor a 0

#Actividad 3
leche = Alimento("Leche", 1500, 10, "30/10/2026")
leche.mostrar_datos()
leche.mostrar_vencimiento()
leche.vender(2)
leche.reponer(4)
print(leche.get_stock())
#escribi reponer en la clase producto
#puede usar ese metodo porque lo hereda de su clase padre
#la diferencia es que reponer() agrega al stock que ya tenemos lo que vamos a reponer y set_stock() lo reemplaza
