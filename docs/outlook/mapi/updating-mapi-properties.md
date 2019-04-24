---
title: Mise à jour des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360514"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="15f41-103">Mise à jour des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="15f41-103">Updating MAPI properties</span></span>

<span data-ttu-id="15f41-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15f41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15f41-105">Les clients et fournisseurs de services peuvent mettre à jour une valeur de propriété en appelant:</span><span class="sxs-lookup"><span data-stu-id="15f41-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="15f41-106">La méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) d'un objet pour mettre à jour la valeur d'une ou plusieurs des propriétés d'un objet.</span><span class="sxs-lookup"><span data-stu-id="15f41-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="15f41-107">La fonction [HrSetOneProp](hrsetoneprop.md) pour mettre à jour une seule propriété à la fois.</span><span class="sxs-lookup"><span data-stu-id="15f41-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="15f41-108">Utilisez **HrSetOneProp** uniquement si l'objet cible est local; Cette fonction peut entraîner une dégradation des performances lorsqu'elle est utilisée avec des objets distants.</span><span class="sxs-lookup"><span data-stu-id="15f41-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="15f41-109">La procédure suivante illustre comment utiliser **SetProps** pour mettre à jour la classe de message ou la propriété PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) d'un message.</span><span class="sxs-lookup"><span data-stu-id="15f41-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="15f41-110">Pour mettre à jour la classe de message d'un message</span><span class="sxs-lookup"><span data-stu-id="15f41-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="15f41-111">AlLouez une structure [SPropValue](spropvalue.md) pour la classe de message et définissez ses membres en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="15f41-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="15f41-112">Appelez la méthode **IMAPIProp:: SetProps** pour définir la nouvelle classe de message.</span><span class="sxs-lookup"><span data-stu-id="15f41-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="15f41-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15f41-113">See also</span></span>

- [<span data-ttu-id="15f41-114">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="15f41-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

