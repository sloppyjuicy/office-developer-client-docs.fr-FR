---
title: Propriété canonique PidTagWizardNoPstPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b94e1f2d66f89d680cc738968342de0fbcee5cda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19786916"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Propriété canonique PidTagWizardNoPstPage

  
  
**S’applique à**: Outlook 
  
Cette propriété contient la valeur TRUE si l’Assistant profil consiste à supprimer la page magasin (PST) des messages personnels.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Identificateur :  <br/> |0x6700  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |D’administration Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Fournisseurs de services peuvent définir cette propriété lors de l’appel d’une fonction basée sur le prototype de la fonction [LAUNCHWIZARDENTRY](launchwizardentry.md) . Cette propriété indique à l’Assistant profil que le fournisseur ne souhaite pas la page PST à afficher au cours de la boîte de dialogue utilisateur. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

