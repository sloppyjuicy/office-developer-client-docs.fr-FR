---
title: Suppression d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
ms.openlocfilehash: 78758550a9b964b73f96c74a0b8d250ed79c6860
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373241"
---
# <a name="deleting-a-recipient"></a>Suppression d’un destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour supprimer une ou plusieurs entrées de carnet d’adresses d’un conteneur modifiable**
  
- Appelez [la méthode IABContainer::D eleteEntries](iabcontainer-deleteentries.md) , en passant un tableau d’identificateurs d’entrée qui représentent les entrées de carnet d’adresses à supprimer. **DeleteEntries peut** renvoyer un avertissement, MAPI_W_PARTIAL_COMPLETION, pour indiquer qu’il n’a pas pu supprimer une ou plusieurs des entrées. Testez cette valeur de retour avec la macro **HR_FAILED** et appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) du conteneur si des informations supplémentaires sur le problème sont nécessaires. 
    
Lorsque vous maintenez un pointeur vers la structure [ADRENTRY](adrentry.md) d’une entrée supprimée dans votre cache, vous pouvez toujours récupérer des propriétés à l’aide de son identificateur d’entrée. Cela est dû au fait que l’entrée est uniquement marquée pour suppression. MAPI conserve un niveau d’accès à ces entrées marquées par conception. 
  

