---
title: Suppression d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421045"
---
# <a name="deleting-a-recipient"></a>Suppression d’un destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour supprimer une ou plusieurs entrées de carnet d’adresses d’un conteneur modifiable**
  
- Appelez [la méthode IABContainer::D eleteEntries,](iabcontainer-deleteentries.md) en passant un tableau d’identificateurs d’entrée qui représentent les entrées de carnet d’adresses à supprimer. **DeleteEntries peut** renvoyer un avertissement, MAPI_W_PARTIAL_COMPLETION, pour indiquer qu’il n’a pas pu supprimer une ou plusieurs des entrées. Testez cette valeur de retour avec la macro **HR_FAILED** et appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) du conteneur si des informations supplémentaires sur le problème sont nécessaires. 
    
Lorsque vous maintenez un pointeur vers la structure [ADRENTRY](adrentry.md) d’une entrée supprimée dans votre cache, vous pouvez toujours récupérer des propriétés à l’aide de son identificateur d’entrée. Cela est dû au fait que l’entrée est uniquement marquée pour suppression. MAPI conserve un niveau d’accès à ces entrées marquées par conception. 
  

