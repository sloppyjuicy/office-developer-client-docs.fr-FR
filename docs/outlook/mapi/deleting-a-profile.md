---
title: Suppression d’un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
ms.openlocfilehash: 1702bdce9126c2582467991a8e7bd4539506e3e1
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520734"
---
# <a name="deleting-a-profile"></a>Suppression d’un profil

**S’applique à** : Outlook 2013 | Outlook 2016
  
 **Pour supprimer un profil**
  
- [Appelez IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md).

 **DeleteProfile marque** le profil à supprimer s’il est en cours d’utilisation, en attendant qu’il ne soit plus actif pour le supprimer. Le profil ne disparaît pas tant que chaque client avec une session active n’a pas été déconnecté.
  
 **DeleteProfile appelle la** fonction de point d’entrée de chaque service de message dans le profil avec le paramètre _ulContext_ paramétré sur MSG_SERVICE_DELETE. Les appels aux fonctions de point d’entrée se produisent avant la suppression physique des services du profil.
  