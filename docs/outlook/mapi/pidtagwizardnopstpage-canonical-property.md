---
title: Propriété canonique PidTagWizardNoPstPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bcf42991c31cfb7313ee1a668b5423db1defbe33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586865"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Propriété canonique PidTagWizardNoPstPage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient TRUE si l’Assistant Profil doit supprimer la page de la boutique de messages personnels (PST).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Identificateur :  <br/> |0x6700  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Exchange Administrative  <br/> |
   
## <a name="remarks"></a>Remarques

Les fournisseurs de services peuvent définir cette propriété lors de l’appel d’une fonction basée sur le prototype de fonction [LAUNCHWIZARDENTRY.](launchwizardentry.md) Cette propriété indique à l’Assistant Profil que le fournisseur ne souhaite pas que la page PST s’affiche pendant la boîte de dialogue utilisateur. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

