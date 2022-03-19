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
ms.openlocfilehash: 4e4554556bbb51007454c6cb1b18ee8903fe3043
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626262"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les opérations de haut niveau sur les objets conteneur tels que les carnets d’adresses, les listes de distribution et les dossiers. Les interfaces [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) et [IDistList : IMAPIContainer](idistlistimapicontainer.md) sont dérivées **d’IMAPIContainer**.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets dossier, conteneur de carnet d’adresses et liste de distribution  <br/> |
|Implémenté par :  <br/> |Magasin de messages, carnet d’adresses et fournisseurs de transport distants  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIContainer  <br/> |
|Type de pointeur :  <br/> |LPMAPICONTAINER  <br/> |
|Modèle de transaction :  <br/> |Classe abstraite, jamais implémentée  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Renvoie un pointeur vers la table des matières du conteneur. |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Renvoie un pointeur vers le tableau hiérarchique du conteneur. |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Ouvre un objet dans le conteneur, renvoyant un pointeur d’interface pour un accès supplémentaire. |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Établit des critères de recherche pour le conteneur. |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Obtient les critères de recherche pour le conteneur. |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
   
## <a name="see-also"></a>Consultez aussi



[Interfaces MAPI](mapi-interfaces.md)

