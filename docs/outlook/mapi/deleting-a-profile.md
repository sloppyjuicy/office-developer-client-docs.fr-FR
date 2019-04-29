---
title: Suppression d'un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410202"
---
# <a name="deleting-a-profile"></a>Suppression d'un profil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour supprimer un profil**
  
- Appeler [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marque le profil pour suppression s'il est en cours d'utilisation, en attendant qu'il ne soit plus actif pour le supprimer. Le profil ne disparaît pas tant que chaque client avec une session active ne s'est pas déconnecté. 
  
 **DeleteProfile** appelle la fonction de point d'entrée de chaque service de messagerie dans le profil avec le paramètre _ULCONTEXT_ défini sur MSG_SERVICE_DELETE. Les appels vers les fonctions de point d'entrée se produisent avant la suppression physique des services du profil. 
  

