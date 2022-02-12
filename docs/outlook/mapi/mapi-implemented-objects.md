---
title: Objets implémentés par MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 51b41db4ccce56f561a1380128b3414e74fe3056
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774775"
---
# <a name="mapi-implemented-objects"></a>Objets implémentés par MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI implémente plusieurs objets pour une utilisation par les applications clientes et les fournisseurs de services. L’objet de session permet aux clients d’utiliser les services de session, d’accéder aux tables et de communiquer avec les fournisseurs de services. L’objet carnet d’adresses fournit aux clients un accès intégré à tous les différents fournisseurs de carnet d’adresses. 
  
MAPI fournit plusieurs objets de table et d’état que les clients peuvent utiliser pour afficher et surveiller les informations de session et de fournisseur de services. Par exemple, MAPI fournit une table de profils avec des informations sur tous les profils installés sur l’ordinateur et une table de service de message avec des informations sur tous les services de message dans le profil actuel. MAPI fournit trois objets d’état différents : un qui représente le sous-système global, un pour lepooler MAPI et un pour le carnet d’adresses intégré. 
  
MAPI implémente quatre objets différents pour la gestion de la configuration des services de messagerie, des fournisseurs de services et des profils. Les clients et les fournisseurs de services utilisent des objets de section d’administration de fournisseur et de profil ; Ces objets leur permettent de configurer des fournisseurs de services et d’accéder aux propriétés de profil. Les clients utilisent uniquement les objets de service de message et d’administration de profil, les objets qui supportent l’administration des profils et des services de message. 
  
MAPI fournit deux objets pour les fournisseurs de services : un objet support et un objet TNEF. Tous les fournisseurs de services utilisent un ou plusieurs objets de prise en charge ; il existe quatre implémentations d’objets de prise en charge différentes. MAPI fournit une implémentation pour prendre en charge la configuration, ainsi que des implémentations spécifiques pour prendre en charge les fournisseurs de carnet d’adresses, de magasin de messages et de transport. L’objet TNEF est utilisé par les fournisseurs de transport qui utilisent le format TNEF (Transport Neutral Encapsulation Format).
  
Deux objets utilitaires, les données de table et les données de propriété, sont généralement utilisés par les fournisseurs de services. Les objets de données de tableau aident à l’implémentation des objets table ; les objets de données de propriété permettent de définir et d’afficher l’accès aux propriétés et l’aide dans l’implémentation [d’IMAPIProp : IUnknown](imapipropiunknown.md), l’interface de propriété de base. 
  
Le tableau suivant résume l’objectif de chaque objet implémenté par MAPI.
  
|**Objet MAPI**|**Description**|
|:-----|:-----|
|Carnet d’adresses  <br/> |Permet d’accéder à l’affichage intégré des informations sur les destinataires qui appartiennent à tous les fournisseurs de carnet d’adresses du profil actif. |
|Administration du service de message  <br/> |Permet d’accéder aux informations de service de message pour la configuration. |
|Administration des profils  <br/> |Permet d’accéder aux informations de profil pour la configuration. |
|Section Profil  <br/> |Partie d’un profil utilisé pour décrire un service de messagerie ou un fournisseur de services particulier. |
|Données de propriété  <br/> |Maintient l’accès aux propriétés et permet **d’implémenter IMAPIProp**. |
|Administration du fournisseur  <br/> |Permet d’accéder aux informations du fournisseur de services pour la configuration. |
|Session  <br/> |Représente une connexion aux systèmes de messagerie sous-jacents et permet aux clients d’accéder aux ressources MAPI. |
|Statut  <br/> |Permet d’accéder à l’état du sous-système MAPI, du carnet d’adresses ou dupooler MAPI. |
|Support  <br/> |Aide les fournisseurs de services à gérer les demandes des clients. |
|Tableau  <br/> |Permet d’accéder à un affichage récapitulatif des données d’objet au format de ligne et de colonne, semblable à une table de base de données. |
|Données de tableau  <br/> |Maintient l’accès aux données de table sous-jacentes et implémente les objets table. |
|TNEF  <br/> |Prend en charge l’utilisation du format TNEF (Transport Neutral Encapsulation Format). |
   
L’illustration suivante montre la relation entre les objets implémentés par MAPI, les interfaces dont ils héritent et les composants qui les utilisent. 
  
**Objets implémentés par MAPI**
  
![Objets implémentés par MAPI](media/amapi_68.gif "Objets implémentés par MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

