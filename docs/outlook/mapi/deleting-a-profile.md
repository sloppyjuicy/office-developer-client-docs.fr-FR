---
title: Suppression d’un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783138"
---
# <a name="deleting-a-profile"></a>Suppression d’un profil

  
  
**S’applique à**: Outlook 
  
 **Pour supprimer un profil**
  
- Appelez [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marque le profil de suppression si elle est actuellement utilisée, en attente jusqu'à ce qu’il n’est plus actif à supprimer. Le profil ne disparaît pas réellement jusqu'à ce que tous les clients avec une session active sont déconnecté. 
  
 **DeleteProfile** appelle la fonction de point d’entrée de chaque service de message dans le profil avec le paramètre _ulContext_ défini sur MSG_SERVICE_DELETE. Les appels aux fonctions de point d’entrée se produisent avant que les services sont physiquement retirés du profil. 
  

