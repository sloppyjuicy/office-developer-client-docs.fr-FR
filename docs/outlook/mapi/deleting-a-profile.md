---
title: Suppression d’un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573242"
---
# <a name="deleting-a-profile"></a>Suppression d’un profil

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour supprimer un profil**
  
- Appelez [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marque le profil de suppression si elle est actuellement utilisée, en attente jusqu'à ce qu’il n’est plus actif à supprimer. Le profil ne disparaît pas réellement jusqu'à ce que tous les clients avec une session active sont déconnecté. 
  
 **DeleteProfile** appelle la fonction de point d’entrée de chaque service de message dans le profil avec le paramètre _ulContext_ défini sur MSG_SERVICE_DELETE. Les appels aux fonctions de point d’entrée se produisent avant que les services sont physiquement retirés du profil. 
  

