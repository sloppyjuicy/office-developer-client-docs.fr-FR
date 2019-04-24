---
title: Copie d'un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285229"
---
# <a name="copying-a-profile"></a>Copie d'un profil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour créer un profil, vous pouvez procéder à une copie à partir d'un profil existant et modifier les services de messagerie et les fournisseurs de services nécessaires. La copie d'un profil implique l'utilisation d'un objet d'administration de profil, fourni par MAPI via la fonction [MAPIAdminProfiles](mapiadminprofiles.md) . 
  
 **Pour copier un profil**
  
1. Appelez **MAPIAdminProfiles** pour récupérer un pointeur d'interface **IProfAdmin** . 
    
2. Appelez [IProfAdmin:: GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profils. 
    
3. Créez une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) au nom du profil à copier. 
    
4. Appelez [IMAPITable:: FindRow](imapitable-findrow.md) pour localiser la ligne appropriée dans la table de profil. 
    
5. Appelez [IProfAdmin:: CopyProfile](iprofadmin-copyprofile.md), en passant la valeur de la colonne **PR_DISPLAY_NAME** en tant que paramètre _lpszOldProfileName_ . 
    

