---
title: Objets implémentés par MAPI
description: Fournit une vue d’ensemble détaillée des objets implémentés par MAPI pour une utilisation par les clients et les fournisseurs de services.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
ms.openlocfilehash: 600f8439f6e716daa25c83973a5a4a76439eecb7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815736"
---
# <a name="mapi-implemented-objects"></a>Objets implémentés par MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI implémente plusieurs objets à utiliser par les applications clientes et les fournisseurs de services. L’objet de session permet aux clients d’utiliser les services de session, d’accéder aux tables et de communiquer avec les fournisseurs de services. L’objet carnet d’adresses fournit aux clients un accès intégré à tous les différents fournisseurs de carnets d’adresses. 
  
MAPI fournit plusieurs objets de table et d’état que les clients peuvent utiliser pour afficher et surveiller les informations de session et de fournisseur de services. Par exemple, MAPI fournit une table de profils avec des informations sur tous les profils installés sur l’ordinateur et une table de service de messages avec des informations sur tous les services de message dans le profil actuel. MAPI fournit trois objets d’état différents : un qui représente le sous-système global, un pour le spouleur MAPI et un pour le carnet d’adresses intégré. 
  
MAPI implémente quatre objets différents pour gérer la configuration des services de message, des fournisseurs de services et des profils. Les clients et les fournisseurs de services utilisent des objets d’administration de fournisseur et de section de profil ; ces objets leur permettent de configurer des fournisseurs de services et des propriétés de profil d’accès. Les clients utilisent uniquement des objets d’administration de profil et de service de message, les objets qui prennent en charge l’administration des services et profils de messages. 
  
MAPI fournit deux objets pour les fournisseurs de services : un objet de support et un objet TNEF. Tous les fournisseurs de services utilisent un ou plusieurs objets de support ; il existe quatre implémentations d’objets de prise en charge différentes. MAPI fournit une implémentation pour prendre en charge la configuration, ainsi que des implémentations spécifiques pour prendre en charge le carnet d’adresses, le magasin de messages et les fournisseurs de transport. L’objet TNEF est utilisé par les fournisseurs de transport qui prennent en charge le format TNEF (Transport Neutral Encapsulation Format).
  
Deux objets utilitaires, les données de table et les données de propriété, sont généralement utilisés par les fournisseurs de services. Les objets de données de table facilitent l’implémentation d’objets de table ; les objets de données de propriété permettent de définir et d’afficher l’accès aux propriétés et d’aider à l’implémentation [d’IMAPIProp : IUnknown](imapipropiunknown.md), l’interface de propriété de base. 
  
Le tableau suivant récapitule l’objectif de chaque objet implémenté par MAPI.
  
|**Objet MAPI**|**Description**|
|:-----|:-----|
|Carnet d’adresses  <br/> |Permet d’accéder à la vue intégrée des informations de destinataire qui appartiennent à tous les fournisseurs de carnets d’adresses dans le profil actif. |
|Administration du service de message  <br/> |Fournit l’accès aux informations de service de message pour la configuration. |
|Administration des profils  <br/> |Fournit l’accès aux informations de profil pour la configuration. |
|Section Profil  <br/> |Partie d’un profil utilisée pour décrire un service de message ou un fournisseur de services particulier. |
|Données de propriété  <br/> |Conserve l’accès aux propriétés et aide à implémenter **IMAPIProp**. |
|Administration du fournisseur  <br/> |Fournit l’accès aux informations du fournisseur de services pour la configuration. |
|Session  <br/> |Représente une connexion aux systèmes de messagerie sous-jacents et fournit aux clients l’accès aux ressources MAPI. |
|Statut  <br/> |Fournit l’accès à l’état du sous-système MAPI, du carnet d’adresses ou du spouleur MAPI. |
|Support  <br/> |Aide les fournisseurs de services à gérer les demandes des clients. |
|Tableau  <br/> |Fournit l’accès à une vue récapitulative des données d’objet au format de ligne et de colonne, similaire à une table de base de données. |
|Données de table  <br/> |Conserve l’accès aux données de table sous-jacentes et implémente les objets de table. |
|TNEF  <br/> |Prend en charge l’utilisation du format TNEF (Transport Neutral Encapsulation Format). |
   
L’illustration suivante montre la relation entre les objets implémentées par MAPI, les interfaces dont ils héritent et les composants qui les utilisent. 
  
**Objets implémentés par MAPI**
  
![Objets implémentés par MAPI](media/amapi_68.gif "Objets implémentés par MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Vue d’ensemble de l’objet et de l’interface MAPI](mapi-object-and-interface-overview.md)

