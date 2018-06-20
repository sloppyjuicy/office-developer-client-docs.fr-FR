---
title: Suppression d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9a3006b43eb9f210603ff3a3d890118e7fd61d7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783137"
---
# <a name="deleting-a-recipient"></a>Suppression d’un destinataire

  
  
**S’applique à**: Outlook 
  
 **Pour supprimer une ou plusieurs entrées de carnet d’adresses d’un conteneur modifiable**
  
- Appelez la méthode [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , en passant un tableau d’identificateurs d’entrée qui représentent les entrées de carnet d’adresses à supprimer. **DeleteEntries** peut renvoyer un avertissement MAPI_W_PARTIAL_COMPLETION se produit, pour indiquer qu’il n’a pas pu supprimer un ou plusieurs des entrées. Testez pour cette valeur de retour à la macro **HR_FAILED** et appeler la méthode de [IMAPIProp::GetLastError](imapiprop-getlasterror.md) du conteneur si plus d’informations sur le problème n’est nécessaire. 
    
Lorsque vous maintenez un pointeur vers la structure [ADRENTRY](adrentry.md) d’une entrée supprimée dans le cache, vous serez toujours en mesure de récupérer les propriétés à l’aide de son identificateur d’entrée. Il s’agit, car l’entrée est uniquement marquée pour suppression. MAPI conserve un niveau d’accès à ces entrées marquées par sa conception. 
  

