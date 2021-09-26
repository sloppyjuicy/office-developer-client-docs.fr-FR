---
title: Copie d’un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4bf3bd7c5d509b0464a620ad0e8a6c00d45b9874
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610999"
---
# <a name="copying-a-profile"></a>Copie d’un profil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’une des façons de créer un profil consiste à copier à partir d’un profil existant et à modifier les services de messagerie et les fournisseurs de services nécessaires. La copie d’un profil implique l’utilisation d’un objet d’administration de profil, fourni par MAPI via la [fonction MAPIAdminProfiles.](mapiadminprofiles.md) 
  
 **Pour copier un profil**
  
1. Appelez **MAPIAdminProfiles** pour récupérer un pointeur d’interface **IProfAdmin.** 
    
2. Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profil. 
    
3. Créez une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom du profil à copier. 
    
4. Appelez [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne appropriée dans la table de profil. 
    
5. Appelez [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), en passant la valeur de la colonne **PR_DISPLAY_NAME** comme paramètre _lpszOldProfileName._ 
    

