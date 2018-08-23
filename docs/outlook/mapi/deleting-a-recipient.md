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
ms.openlocfilehash: 03917ad52f1dc1ce4d0b59cd54fe33f58f352061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582944"
---
# <a name="deleting-a-recipient"></a>Suppression d’un destinataire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour supprimer une ou plusieurs entrées de carnet d’adresses d’un conteneur modifiable**
  
- Appelez la méthode [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , en passant un tableau d’identificateurs d’entrée qui représentent les entrées de carnet d’adresses à supprimer. **DeleteEntries** peut renvoyer un avertissement MAPI_W_PARTIAL_COMPLETION se produit, pour indiquer qu’il n’a pas pu supprimer un ou plusieurs des entrées. Testez pour cette valeur de retour à la macro **HR_FAILED** et appeler la méthode de [IMAPIProp::GetLastError](imapiprop-getlasterror.md) du conteneur si plus d’informations sur le problème n’est nécessaire. 
    
Lorsque vous maintenez un pointeur vers la structure [ADRENTRY](adrentry.md) d’une entrée supprimée dans le cache, vous serez toujours en mesure de récupérer les propriétés à l’aide de son identificateur d’entrée. Il s’agit, car l’entrée est uniquement marquée pour suppression. MAPI conserve un niveau d’accès à ces entrées marquées par sa conception. 
  

