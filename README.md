# Alhaja_Garcia_Carmen_XML
EXPLICACIÓN ¿POR QUÉ HE DECIDIDO ESTE DISEÑO?

1. Contraseña de Seguridad
"La contraseña debe contener, al menos, 8 caracteres, incluyendo mayúsculas, minúsculas, dígitos y símbolos. Al igual que el anterior, investiga cuáles son los estándares que se utiliza para este aspecto y justifica tu elección."

He escogido este patrón [a-zA-Z0-9\W_]{8,} porque es compatible con el motor de validación de XML Schema (W3C), asegura que tenga minimo 8 caracteres y permite mayúsculas, minusculas, números y símbolos.

2. Número de teléfono
"El número de teléfono debe seguir un formato específico. Para esto, investiga cuál es el formato oficial y la numeración específica española."

He escogido este patrón [6789][0-9]{8} de número de teléfono porque pertenece al Plan Nacional de Numeración de España y establece que los números tienen 9 dígitos. Los rangos oficiales Españoles obligan a que el primer caracter sea 6, 7, 8 o 9, seguido de 8 dígitos numéricos adicionales.

3. Código Postal
"El código postal debe ajustarse a un patrón específico de 5 dígitos. Para esto, investiga cuáles son los números que se utilizan en España para la codificación postal."

He escogido el patrón (0[1-9]|[1-4][0-9]|5[0-2])[0-9]{3} de código postal porque consta de 5 dígitos. Los dos primeros identifican la provincia (01-52), que va de la provincia 1 a la 52. 

4. Nombre de Usuario
"Nombre de usuario debe comenzar con una letra minúscula y permitir solo ciertos caracteres alfanuméricos. Investiga sobre los estándares que permiten este diseño."

He escogido el patrón [a-z][a-zA-Z0-9]* porque los estandares de nomenclatura suelen exigir que el primer caracter sea una letra minuscula para evitar errores sintácticos y así permitir que el resto de dígitos sean números. Por eso la [a-z] obliga que la primera sea una letra cualquiera en minúscula y el resto [a-zA-Z0-9]* lo puedes eligir mas libremente.

5. Correo electrónico
"El correo electrónico debe cumplir con un formato estándar. Para esto, investiga cuáles son los caracteres permitidos para construir direcciones de correo electrónico."

Según el estándar de RFC 5322, se permiten caracteres alfanumericos y ciertos símbolos especiales (., _, %, +, -) antes de la arroba (@). He usado el patrón [a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,} porque garantiza que la dirección tenga un nombre de usuario válido, el símbolo de arroba, un dominio y una extensión de al menos dos letras.
