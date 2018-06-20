---
title: Copie d’un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 77c7853c07830804aaa044f08078d95785bcfda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783073"
---
# <a name="copying-a-profile"></a>Copie d’un profil

  
  
**S’applique à**: Outlook 
  
Pour créer un profil consiste à copier un profil existant et de modifier les fournisseurs de services et les services de messagerie nécessaires. Copie d’un profil implique l’utilisation d’un objet d’administration de profil, fourni par MAPI par le biais de la fonction [MAPIAdminProfiles](mapiadminprofiles.md) . 
  
 **Pour copier un profil**
  
1. Appelez **MAPIAdminProfiles** pour récupérer un pointeur d’interface **IProfAdmin** . 
    
2. Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profils. 
    
3. Créer une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) correspondre **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom du profil à copier. 
    
4. Appel [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne appropriée dans la table de profils. 
    
5. Appelez [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), en passant la valeur de la colonne **PR_DISPLAY_NAME** en tant que paramètre _lpszOldProfileName_ . 
    

