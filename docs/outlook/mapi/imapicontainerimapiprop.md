---
title: IMAPIContainer IMAPIProp
description: IMAPIContainerIMAPIProp gère les opérations générales sur les objets conteneur tels que les carnets d’adresses, les listes de distribution et les dossiers.
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
ms.openlocfilehash: 5790ef6fa12a8fdb297164d1c9f233bc3bf2d08b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817871"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les opérations générales sur les objets conteneur tels que les carnets d’adresses, les listes de distribution et les dossiers. Les interfaces [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) et [IDistList : IMAPIContainer](idistlistimapicontainer.md) sont dérivées d’IMAPIContainer.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Dossier, conteneur de carnet d’adresses et objets de liste de distribution  <br/> |
|Implémenté par :  <br/> |Magasin de messages, carnet d’adresses et fournisseurs de transport à distance  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIContainer  <br/> |
|Type de pointeur :  <br/> |LPMAPICONTAINER  <br/> |
|Modèle de transaction :  <br/> |Classe abstraite, jamais implémentée  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Retourne un pointeur vers la table du contenu du conteneur. |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Retourne un pointeur vers la table de hiérarchie du conteneur. |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Ouvre un objet dans le conteneur, en retournant un pointeur d’interface pour un accès supplémentaire. |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Établit des critères de recherche pour le conteneur. |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Obtient les critères de recherche pour le conteneur. |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

