---
title: Suppression d'un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316813"
---
# <a name="deleting-a-recipient"></a>Suppression d'un destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour supprimer une ou plusieurs entrées de carnet d'adresses d'un conteneur modifiable**
  
- Appelez la méthode [IABContainer::D eleteentries](iabcontainer-deleteentries.md) , en passant un tableau d'identificateurs d'entrée qui représentent les entrées de carnet d'adresses à supprimer. **DeleteEntries** peut renvoyer un avertissement, MAPI_W_PARTIAL_COMPLETION, pour indiquer qu'il n'a pas pu supprimer une ou plusieurs entrées. Testez cette valeur de retour avec la macro **HR_FAILED** et appelez la méthode [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) du conteneur si davantage d'informations sur le problème sont nécessaires. 
    
Lorsque vous placez un pointeur sur la structure [ADRENTRY](adrentry.md) d'une entrée supprimée dans votre cache, vous pouvez toujours récupérer les propriétés à l'aide de son identificateur d'entrée. Cela est dû au fait que l'entrée est uniquement marquée pour suppression. MAPI conserve un niveau d'accès à ces entrées marquées par la conception. 
  

