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
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407521"
---
# <a name="updating-mapi-properties"></a>Mise à jour des propriétés MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients et les fournisseurs de services peuvent mettre à jour une valeur de propriété en appelant :
  
- Méthode [IMAPIProp::SetProps](imapiprop-setprops.md) d’un objet pour mettre à jour la valeur d’une ou de plusieurs propriétés d’un objet. 
    
- Fonction [HrSetOneProp](hrsetoneprop.md) pour mettre à jour une seule propriété à la fois. Utilisez **HrSetOneProp** uniquement si l’objet cible est local ; Cette fonction peut entraîner une dégradation des performances lorsqu’elle est utilisée avec des objets distants. 
    
La procédure suivante montre comment utiliser **SetProps** pour mettre à jour la classe de message, ou la propriété PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), d’un message. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Pour mettre à jour la classe de message d’un message 
  
1. Allouez une structure [SPropValue](spropvalue.md) pour la classe de message et définissez ses membres selon le cas. 
    
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

