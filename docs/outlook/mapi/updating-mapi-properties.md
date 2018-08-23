---
title: Mise à jour des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 172abe64073b11d98bfb5f76999237218ef8944a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581348"
---
# <a name="updating-mapi-properties"></a>Mise à jour des propriétés MAPI

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Clients et fournisseurs de services peuvent mettre à jour une valeur de propriété en appelant :
  
- Méthode [IMAPIProp::SetProps](imapiprop-setprops.md) d’un objet à mettre à jour la valeur d’une ou plusieurs des propriétés d’un objet. 
    
- La fonction [HrSetOneProp](hrsetoneprop.md) pour mettre à jour qu’une seule propriété à la fois. Utilisez **HrSetOneProp** uniquement si l’objet cible est local ; Cette fonction peut entraîner une dégradation des performances lorsqu’elle est utilisée avec des objets distants. 
    
La procédure suivante illustre comment utiliser **SetProps** pour mettre à jour la classe de message, ou la propriété PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) d’un message. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Pour mettre à jour de la classe de message d’un message 
  
1. Allouer une structure [SPropValue](spropvalue.md) pour la classe de message et définir ses membres comme il convient. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Appelez la méthode **IMAPIProp::SetProps** du message pour définir la nouvelle classe de message. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

