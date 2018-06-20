---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783701"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**S’applique à**: Outlook 
  
Gère les opérations de haut niveau sur les objets conteneur tels que des carnets d’adresses, des listes de distribution et des dossiers. La [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), et [IDistList : IMAPIContainer](idistlistimapicontainer.md) **IMAPIContainer**proviennent des interfaces.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Dossier conteneur de carnet d’adresses et les objets de liste de distribution  <br/> |
|Implémentée par :  <br/> |Banque de messages, carnet d’adresses et fournisseurs de transport à distance  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIContainer  <br/> |
|Type de pointeur :  <br/> |LPMAPICONTAINER  <br/> |
|Modèle de transaction :  <br/> |Classe abstraite, jamais implémentée  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Retourne un pointeur vers la table des matières du conteneur.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Retourne un pointeur vers la table de hiérarchie du conteneur.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Ouvre un objet dans le conteneur, en retournant un pointeur d’interface pour l’accès des autres.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Définit les critères de recherche pour le conteneur.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Obtient les critères de recherche pour le conteneur.  <br/> |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

