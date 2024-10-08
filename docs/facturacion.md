
## Tasklists fact

- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque


# FACTURACION Y COSTOS ASDLEKLKWQEM

A continuación se muestra el diagrama de arquitectura que ilustra cómo interactúan los diferentes componentes en Azure.

- **Flujo de datos**: Los usuarios acceden a la aplicación web a través del Application Gateway, que dirige el tráfico a App Service. Las solicitudes para almacenar o recuperar datos pasan por el SQL Database y Blob Storage.
- **Alta disponibilidad**: Azure Traffic Manager garantiza la disponibilidad del servicio dirigiendo el tráfico entre múltiples regiones en caso de falla.

![Diagrama de Arquitectura](images/azure-web-architecture.png)

El diagrama muestra la interacción de los siguientes componentes:
1. Usuarios
2. Azure Traffic Manager
3. Azure App Service
4. Azure SQL Database
5. Azure Blob Storage
6. Azure Virtual Network (VNet)
7. Azure Key Vault