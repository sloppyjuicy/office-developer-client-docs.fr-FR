---
title: Objets implémentés par MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 86aa8451b5b127764134f1a3a905366fd014d0c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346853"
---
# <a name="mapi-implemented-objects"></a>Objets implémentés par MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI implémente plusieurs objets pour les applications clientes et les fournisseurs de services. L'objet session permet aux clients d'utiliser des services de session, d'accéder à des tables et de communiquer avec des fournisseurs de services. L'objet carnet d'adresses fournit aux clients un accès intégré à tous les différents fournisseurs de carnet d'adresses. 
  
MAPI fournit plusieurs objets table et Status que les clients peuvent utiliser pour afficher et surveiller les informations des fournisseurs de services et de session. Par exemple, MAPI fournit une table de profil contenant des informations sur tous les profils installés sur l'ordinateur et une table de service de message contenant des informations sur tous les services de messagerie dans le profil actuel. MAPI fournit trois objets d'état différents: un qui représente le sous-système global, un pour le spouleur MAPI et un autre pour le carnet d'adresses intégré. 
  
MAPI implémente quatre objets différents pour la gestion de la configuration des services de messagerie, des fournisseurs de services et des profils. Les clients et les fournisseurs de services utilisent les objets de section de profil et d'administration du fournisseur; ces objets leur permettent de configurer des fournisseurs de services et d'accéder aux propriétés de profil. Les clients utilisent uniquement les objets de service de messagerie et d'administration de profil, les objets qui prennent en charge l'administration des services de message et des profils. 
  
MAPI fournit deux objets pour les fournisseurs de services: un objet de prise en charge et un objet TNEF. Tous les fournisseurs de services utilisent un ou plusieurs objets de prise en charge; Il existe quatre implémentations d'objet de prise en charge différentes. MAPI fournit une implémentation pour prendre en charge la configuration, ainsi que des implémentations spécifiques pour prendre en charge les fournisseurs de carnet d'adresses, de banque de messages et de transport. L'objet TNEF est utilisé par les fournisseurs de transport qui prennent en charge le format TNEF (Transport Neutral Encapsulation Format).
  
Deux objets utilitaire, les données de table et les données de propriété, sont généralement utilisés par les fournisseurs de services. Les objets de données de tableau permettent d'implémenter des objets de tableau; les objets de données de propriété permettent de définir et d'afficher l'accès aux propriétés et de l'aide dans l'implémentation de [IMAPIProp: IUnknown](imapipropiunknown.md), l'interface de propriété de base. 
  
Le tableau suivant résume l'objectif de chaque objet implémenté par MAPI.
  
|**Objet MAPI**|**Description**|
|:-----|:-----|
|Carnet d’adresses  <br/> |Permet d'accéder à l'affichage intégré des informations sur le destinataire qui appartiennent à tous les fournisseurs de carnets d'adresses dans le profil actif.  <br/> |
|Administration du service de messagerie  <br/> |Fournit l'accès aux informations du service de messagerie pour la configuration.  <br/> |
|Administration des profils  <br/> |Fournit l'accès aux informations de profil pour la configuration.  <br/> |
|Section Profil  <br/> |Partie d'un profil utilisée pour décrire un service de messagerie ou un fournisseur de services particulier.  <br/> |
|Données de propriété  <br/> |Conserve l'accès aux propriétés et permet d'implémenter **IMAPIProp**.  <br/> |
|Administration des fournisseurs  <br/> |Fournit l'accès aux informations du fournisseur de services pour la configuration.  <br/> |
|Session  <br/> |Représente une connexion aux systèmes de messagerie sous-jacents et permet aux clients d'accéder aux ressources MAPI.  <br/> |
|Statut  <br/> |Permet d'accéder à l'état du sous-système MAPI, du carnet d'adresses ou du spouleur MAPI.  <br/> |
|Support  <br/> |Permet aux fournisseurs de services de gérer les demandes des clients.  <br/> |
|Table  <br/> |Permet d'accéder à une vue récapitulative des données d'objet dans le format de ligne et de colonne, semblable à une table de base de données.  <br/> |
|Données de tableau  <br/> |Conserve l'accès aux données de la table sous-jacente et implémente les objets table.  <br/> |
|TNEF  <br/> |Prend en charge l'utilisation du format TNEF (Transport Neutral Encapsulation Format).  <br/> |
   
L'illustration suivante montre la relation entre les objets implémentés par MAPI, les interfaces dont ils héritent et les composants qui les utilisent. 
  
**Objets implémentés par MAPI**
  
![Objets implémentés par MAPI] (media/amapi_68.gif "Objets implémentés par MAPI")
  
## <a name="see-also"></a>Voir aussi

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Vue d'ensemble de l'objet et de l'interface MAPI](mapi-object-and-interface-overview.md)

