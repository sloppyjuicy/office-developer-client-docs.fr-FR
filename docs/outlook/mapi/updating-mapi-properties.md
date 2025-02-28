---
title: Mise à jour des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
ms.openlocfilehash: f9aa404503b4932ce60ed15815334ca4e5216794
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378519"
---
# <a name="updating-mapi-properties"></a>Mise à jour des propriétés MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients et les fournisseurs de services peuvent mettre à jour une valeur de propriété en appelant :
  
- Méthode [IMAPIProp::SetProps](imapiprop-setprops.md) d’un objet pour mettre à jour la valeur d’une ou de plusieurs propriétés d’un objet. 
    
- Fonction [HrSetOneProp](hrsetoneprop.md) pour mettre à jour une seule propriété à la fois. Utilisez **HrSetOneProp** uniquement si l’objet cible est local ; Cette fonction peut entraîner une dégradation des performances lorsqu’elle est utilisée avec des objets distants. 
    
La procédure suivante montre comment utiliser **SetProps** pour mettre à jour la classe de message ou la propriété PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) d’un message. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Pour mettre à jour la classe de message d’un message 
  
1. Allouez [une structure SPropValue](spropvalue.md) pour la classe de message et définissez ses membres selon le cas. 
    
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

