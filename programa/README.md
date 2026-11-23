# Programa de referencia para Playground

Copia del programa `registro` de WayLearn, con Registro, Cliente y Venta. La procedencia y revisión están en `docs/ORIGENES.md`.

- `src/lib.rs`: programa de referencia sin modificar.
- `client/client.ts`: cliente de referencia para Solana Playground.

Esta carpeta no es un workspace Anchor CLI completo. El `declare_id!("")` de la fuente es el marcador del material de Playground; el proyecto de Playground debe gestionar la dirección real del programa antes de compilar y desplegar.

Para conectar el frontend, utiliza el IDL exportado del código que realmente desplegaste. Sigue `docs/IDL-Y-PLAYGROUND.md`. Si ya trabajas con el programa en el repositorio canónico o en Playground, no necesitas reemplazarlo por esta copia.

---

# VentasChain — Proyecto final Advanced Bootcamp

## Descripción

VentasChain es una aplicación de registro de ventas
desarrollada con tecnologías de Solana.

Permite administrar negocios, registrar clientes,
guardar ventas, corregir importes y gestionar devoluciones.

El proyecto utiliza un programa en Rust con Anchor
y una interfaz web desarrollada con React y TypeScript.

## Ruta elegida

Proyecto guiado, basado en el material educativo de WayLearn.

Se utilizó el proyecto Registro-Ventas-Solana-App
como punto de partida para desarrollar mejoras propias.

## Aportaciones propias

Las mejoras realizadas para VentasChain son:

1. Personalización del nombre de la aplicación.
2. Configuración del negocio inicial "Tienda Aylin".
3. Incorporación de un resumen de clientes registrados.
4. Cálculo del número de ventas activas.
5. Cálculo del importe total de ventas activas.
6. Implementación de un buscador de clientes por nombre.

Los indicadores se calculan utilizando los datos
consultados del registro, sin inventar información.

## Tecnologías utilizadas

- Solana
- Rust
- Anchor
- React
- TypeScript
- Vite
- GitHub Codespaces

## Archivos principales

- `programa/src/lib.rs`: programa desarrollado con Anchor.
- `src/components/Registro.tsx`: pantalla de clientes y ventas.
- `src/components/Conexion.tsx`: conexión con Solana.
- `src/config/interfaz.ts`: personalización de la aplicación.
- `src/solana/`: funciones de comunicación con Solana.
- `idl.json`: descripción del programa Anchor.
- `clients/js/`: cliente TypeScript del programa.

## Cómo ejecutar el proyecto

Se requiere Node.js 22 y npm.

1. Descargar o clonar el repositorio.
2. Abrir una terminal en la carpeta del proyecto.
3. Instalar las dependencias:

   npm ci

4. Iniciar la aplicación:

   npm run dev

5. Abrir la dirección indicada por Vite.
   En Codespaces se utiliza el puerto 5173.

## Pruebas realizadas

Se ejecutó el comando:

   npm run verificar

La verificación del código y la compilación
del frontend finalizaron correctamente.

También se comprobó visualmente que aparecen
el resumen de ventas y el buscador de clientes.

## Estado del despliegue

Red de desarrollo: Solana Devnet.

El programa Rust compiló correctamente en
Solana Playground.

El despliegue en Devnet está pendiente porque
la billetera todavía no dispone de SOL de prueba.

La aplicación conserva temporalmente el IDL
de referencia del material del curso.

Las operaciones reales del registro permanecerán
bloqueadas hasta importar el IDL correspondiente
a un programa desplegado y verificar transacciones.

Program ID desplegado en Devnet: PENDIENTE.

## Identificación

Nombre: Aylin Jaimes

Correo utilizado en el bootcamp: jaimesaylin002@gmail.com

## Créditos

Proyecto desarrollado a partir del material educativo
del Advanced Bootcamp de WayLearn.

Personalización y mejoras: Aylin Jaimes.

