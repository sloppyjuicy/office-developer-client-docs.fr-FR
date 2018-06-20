---
title: Mise à jour des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787408"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="77bd1-103">Mise à jour des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="77bd1-103">Updating MAPI properties</span></span>

<span data-ttu-id="77bd1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77bd1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77bd1-105">Clients et fournisseurs de services peuvent mettre à jour une valeur de propriété en appelant :</span><span class="sxs-lookup"><span data-stu-id="77bd1-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="77bd1-106">Méthode [IMAPIProp::SetProps](imapiprop-setprops.md) d’un objet à mettre à jour la valeur d’une ou plusieurs des propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="77bd1-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="77bd1-107">La fonction [HrSetOneProp](hrsetoneprop.md) pour mettre à jour qu’une seule propriété à la fois.</span><span class="sxs-lookup"><span data-stu-id="77bd1-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="77bd1-108">Utilisez **HrSetOneProp** uniquement si l’objet cible est local ; Cette fonction peut entraîner une dégradation des performances lorsqu’elle est utilisée avec des objets distants.</span><span class="sxs-lookup"><span data-stu-id="77bd1-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="77bd1-109">La procédure suivante illustre comment utiliser **SetProps** pour mettre à jour la classe de message, ou la propriété PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) d’un message.</span><span class="sxs-lookup"><span data-stu-id="77bd1-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="77bd1-110">Pour mettre à jour de la classe de message d’un message</span><span class="sxs-lookup"><span data-stu-id="77bd1-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="77bd1-111">Allouer une structure [SPropValue](spropvalue.md) pour la classe de message et définir ses membres comme il convient.</span><span class="sxs-lookup"><span data-stu-id="77bd1-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="77bd1-112">Appelez la méthode **IMAPIProp::SetProps** du message pour définir la nouvelle classe de message.</span><span class="sxs-lookup"><span data-stu-id="77bd1-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="77bd1-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77bd1-113">See also</span></span>

- [<span data-ttu-id="77bd1-114">Vue d'ensemble de la propri�t� MAPI</span><span class="sxs-lookup"><span data-stu-id="77bd1-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

