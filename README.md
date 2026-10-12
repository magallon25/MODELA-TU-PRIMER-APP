# MODELA-TU-PRIMER-APP
graph LR
    subgraph Sistema_Cafeteria ["Límite del Sistema: App Cafetería"]
        CU1(("Consultar menú"))
        CU2(("Hacer pedido"))
        CU3(("Pagar"))
        CU4(("Preparar pedido"))
        CU5(("Notificar pedido listo"))

        CU2 -. "«include»" .-> CU3
    end

    Alumno["Actor: Alumno"] --- CU1
    Alumno --- CU2

    CU4 --- Personal["Actor: Personal de cafetería"]
    CU5 --- Personal
