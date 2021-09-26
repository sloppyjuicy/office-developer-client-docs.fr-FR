---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5a76b5cb08e098235dda03df81becf9b15c6ee69
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610656"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les opérations de haut niveau sur les objets conteneur tels que les carnets d’adresses, les listes de distribution et les dossiers. Les interfaces [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)et [IDistList : IMAPIContainer](idistlistimapicontainer.md) sont dérivées d’IMAPIContainer . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets dossier, conteneur de carnet d’adresses et liste de distribution  <br/> |
|Implémenté par :  <br/> |Magasin de messages, carnet d’adresses et fournisseurs de transport distant  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIContainer  <br/> |
|Type de pointeur :  <br/> |LPMAPICONTAINER  <br/> |
|Modèle de transaction :  <br/> |Classe abstraite, jamais implémentée  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Renvoie un pointeur vers la table des matières du conteneur.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Renvoie un pointeur vers le tableau hiérarchique du conteneur.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Ouvre un objet dans le conteneur, renvoyant un pointeur d’interface pour un accès supplémentaire.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Établit des critères de recherche pour le conteneur.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Obtient les critères de recherche pour le conteneur.  <br/> |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

