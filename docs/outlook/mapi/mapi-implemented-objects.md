---
title: Objets implémentés de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d212a86aae0503a5e02a5a7ecddb83db10a4d664
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572374"
---
# <a name="mapi-implemented-objects"></a>Objets implémentés de MAPI
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI implémente plusieurs objets pour une utilisation par les applications clientes et des fournisseurs de services. L’objet session permet aux clients d’utiliser les services de session, pour accéder aux tables et de communiquer avec les fournisseurs de services. L’objet de carnet d’adresses fournit aux clients avec accès intégré à tous les fournisseurs de carnet d’adresses différent. 
  
MAPI fournit plusieurs objets de table et l’état pour les clients à utiliser pour l’affichage et les informations de fournisseur session et le service de surveillance. Par exemple, MAPI fournit une table de profil avec des informations sur tous les profils qui sont installés sur l’ordinateur et une table de service de message avec des informations sur tous les services de message dans le profil actif. MAPI propose trois objets différents états disponibles : un objet représentant le sous-système global, un pour le spouleur MAPI et un pour le carnet d’adresses intégré. 
  
MAPI implémente quatre objets différents pour la gestion de la configuration des services de messagerie, les fournisseurs de services et les profils. Les clients et les fournisseurs de services utilisent administration du fournisseur et les objets de section de profil ; ces objets leur permettant d’accéder aux propriétés de profil et de configurer les fournisseurs de services. Les clients utilisent le service de message uniquement et objets d’administration de profil, les objets qui prennent en charge l’administration des services de messagerie et les profils. 
  
MAPI fournit deux objets pour les fournisseurs de services : un objet de prise en charge et un objet TNEF. Tous les fournisseurs de services utilisent un ou plusieurs objets de prise en charge ; Il existe quatre implémentations d’objets de prise en charge différentes. MAPI fournit une implémentation pour prendre en charge la configuration, ainsi que des implémentations spécifiques pour prendre en charge des fournisseurs de transport, banque de messages et du carnet d’adresses. L’objet TNEF est utilisé par les fournisseurs de transport qui prennent en charge le Transport Neutral Encapsulation Format TNEF ().
  
Deux objets utilitaires, des données de table et les données de propriété sont généralement utilisés par les fournisseurs de services. Objets de données de table de vous aider à l’implémentation de l’objet table ; propriété données objets aide et accès à la propriété set et afficher plus d’informations sur l’implémentation de [IMAPIProp : IUnknown](imapipropiunknown.md), l’interface de la propriété de base. 
  
Le tableau suivant résume l’objectif de chaque objet qui implémente MAPI.
  
|**Objet MAPI**|**Description**|
|:-----|:-----|
|Carnet d’adresses  <br/> |Permet d’accéder à la vue intégrée des informations de destinataire qui appartient à tous les fournisseurs de carnet d’adresses dans le profil actif.  <br/> |
|Administration du service de message  <br/> |Permet d’accéder aux informations de service de message pour la configuration.  <br/> |
|Administration des profils  <br/> |Donne accès aux informations de profil pour la configuration.  <br/> |
|Section de profil  <br/> |Une partie d’un profil utilisé pour décrire un service de message particulier ou d’un fournisseur de services.  <br/> |
|Données de propriété  <br/> |Gère l’accès aux propriétés et vous aide à mettre en œuvre **IMAPIProp**.  <br/> |
|Administration du fournisseur  <br/> |Fournit l’accès aux informations de fournisseur de service de configuration.  <br/> |
|Session  <br/> |Représente une connexion à des systèmes de messagerie sous-jacentes et fournit aux clients d’accéder aux ressources MAPI.  <br/> |
|Status  <br/> |Permet d’accéder à l’état du sous-système MAPI, le carnet d’adresses ou le spouleur MAPI.  <br/> |
|Support  <br/> |Permet de fournisseurs de services de gérer les demandes des clients.  <br/> |
|Table  <br/> |Permet d’accéder à un affichage de synthèse des données d’objet dans un format de ligne et de colonne, similaire à une table de base de données.  <br/> |
|Données de la table  <br/> |Gère l’accès aux données de la table sous-jacente et implémente les objets table.  <br/> |
|TNEF  <br/> |Prend en charge l’utilisation de la Neutral Encapsulation Format TNEF (Transport).  <br/> |
   
L’illustration suivante montre la relation entre les objets que MAPI implémente les interfaces à partir de laquelle ils héritent et les composants qui les utilisent. 
  
**Objets implémentés par MAPI**
  
![Objets implémentés par MAPI] (media/amapi_68.gif "Objets implémentés par MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

