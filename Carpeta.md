function Mostrar-Menu {
    Clear-Host
    Write-Host "Calculadora básica"
    Write-Host "1. Suma"
    Write-Host "2. Resta"
    Write-Host "3. Multiplicación"
    Write-Host "4. División"
    Write-Host "5. Salir"
}

do {
    Mostrar-Menu
    $opcion = Read-Host "Selecciona una opción"

    switch ($opcion) {
        1 {
            $num1 = Read-Host "Ingresa el primer número"
            $num2 = Read-Host "Ingresa el segundo número"
            $resultado = [double]$num1 + [double]$num2
            Write-Host "El resultado de la suma es: $resultado"
            pause
        }
        2 {
            $num1 = Read-Host "Ingresa el primer número"
            $num2 = Read-Host "Ingresa el segundo número"
            $resultado = [double]$num1 - [double]$num2
            Write-Host "El resultado de la resta es: $resultado"
            pause
        }
        3 {
            $num1 = Read-Host "Ingresa el primer número"
            $num2 = Read-Host "Ingresa el segundo número"
            $resultado = [double]$num1 * [double]$num2
            Write-Host "El resultado de la multiplicación es: $resultado"
            pause
        }
        4 {
            $num1 = Read-Host "Ingresa el numerador"
            do {
                $num2 = Read-Host "Ingresa el denominador"
                if ([double]$num2 -eq 0) {
                    Write-Host "Error: No puedes dividir por cero. Ingresa un denominador diferente de 0."
                }
            } while ([double]$num2 -eq 0)
            
            $resultado = [double]$num1 / [double]$num2
            Write-Host "El resultado de la división es: $resultado"
            pause
        }
        5 {
            Write-Host "Saliendo de la calculadora."
            break
        }
        default {
            Write-Host "Opción no válida. Por favor, selecciona una opción válida."
        }
    }
} while ($true)
