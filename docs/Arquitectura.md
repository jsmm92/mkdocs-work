# Arquitectura Azure SDS

### Topología Modelo Hub and Spoke Azure SDS

Para la SDS, se diseñó e implementó una topología de red y seguridad basada en el modelo Hub and Spoke, siguiendo las recomendaciones del Cloud Adoption Framework (CAF) de Azure. Esta topología permite trabajar de manera flexible y segura en la implementación de aplicaciones y recursos. El diseño comprende la gestión de los recursos perimetrales (seguridad, VPN y acceso remoto) en el hub, mientras que los servicios se despliegan en los spokes.

[Fuente Documentacion Microsoft Azure Hub and Spoke](https://learn.microsoft.com/es-es/azure/architecture/networking/architecture/hub-spoke?tabs=cli){:target="_blank"}

Acontinuación se muestra el diagrama implementado en la nube Azure de la SDS, tanto para los recursos de los ambiente producción como para desarrollo.

## Topología Hub And Spoke Ambiente Producción:

![Topologia Hub And Spoke Ambiente Prod](imagenes/hubandspokeprod.png)

### Caracteristicas de este modelo para ambiente productivo

- [x] Se cuenta con una Vnet Hub y VPN Gateway el cual permite la conectividad de servicios desde onpremise hacia la Nube y visceversa.
- [x] Esta presente el emparejamiento de redes para la conectividad mediante vnets, subnets y suscripciones dosponibles.
- [x] Se implemento el servicio de Azure Firewall para filtrar el trafico y proteger la red interna del hub.
- [x] Se cuenta con un recurso de Azure Bastion para conectividad a VMs evitando exposicion directa a internet.
- [x] Se implemento el servicio de Azure Front Door para enrutar el trafico mejorando la disponibilidad y seguridad mediante el WAF que ofrece.

## Topología Hub And Spoke Ambiente Dev:

![Topologia Hub And Spoke Ambiente Dev](imagenes/hubandspokedev.png)

### Caracteristicas de este modelo para ambiente Dev Test

- [x] Se cuenta con una Vnet Hub y VPN Gateway el cual permite la conectividad de servicios desde onpremise hacia la Nube y visceversa.
- [x] Esta presente el emparejamiento de redes para la conectividad mediante vnets, subnets y suscripciones dosponibles.
- [x] Se implemento el servicio de Azure Firewall para filtrar el trafico y proteger la red interna del hub.
- [x] Se cuenta con un recurso de Azure Bastion para conectividad a VMs evitando exposicion directa a internet.
- [x] Se implemento el servicio de Azure Front Door para enrutar el trafico mejorando la disponibilidad y seguridad mediante el WAF que ofrece.

# Descripción General de la Arquitectura Web en Azure

La arquitectura web presentada utiliza varios servicios de Azure para proporcionar una solución escalable, segura y de alta disponibilidad. A continuación se muestra una descripción de los componentes clave.

## Componentes Clave:

1. **Azure App Service**: Aloja la aplicación web y permite una fácil escalabilidad.
2. **Azure SQL Database**: Proporciona una base de datos relacional en la nube.
3. **Azure Blob Storage**: Almacena archivos estáticos y contenido multimedia.
4. **Azure Traffic Manager**: Dirige el tráfico entre múltiples regiones para garantizar alta disponibilidad.
5. **Azure Application Gateway**: Actúa como balanceador de carga y firewall de aplicaciones web (WAF).
6. **Azure Virtual Network (VNet)**: Proporciona una red segura para conectar los servicios.
7. **Azure Key Vault**: Gestiona los secretos, claves y certificados de la aplicación.
