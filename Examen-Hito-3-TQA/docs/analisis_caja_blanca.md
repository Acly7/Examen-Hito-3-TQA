# Análisis de caja blanca

```python
def validar_compra(edad, cuenta_activa, saldo, monto):
    if edad < 18:
        return "Compra no permitida: edad"
    if not cuenta_activa:
        return "Compra no permitida: cuenta"
    if saldo >= monto and monto > 0:
        return "Compra aprobada"
    return "Compra rechazada"
```

Decisiones: D1 edad<18; D2 not cuenta_activa; D3 saldo>=monto and monto>0. Condiciones simples C1, C2, C3 y C4.

Criterio: cobertura de decisiones. Mínimo: **4 casos** para alcanzar los cuatro retornos mutuamente excluyentes.

- CB-01 (16, True, 100, 50): Compra no permitida: edad; D1 verdadero.
- CB-02 (20, False, 100, 50): Compra no permitida: cuenta; D1 falso, D2 verdadero.
- CB-03 (20, True, 100, 50): Compra aprobada; D1 falso, D2 falso, D3 verdadero.
- CB-04 adicional (20, True, 10, 50): Compra rechazada; D3 falso.

Para condiciones simples también probar monto=0 con saldo=100, edad=20 y cuenta activa, para que C4 sea falsa habiéndose evaluado.
