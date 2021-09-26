---
title: Propriété canonique PidTagWizardNoPabPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f66afac0d76705eb2a7910310626097cd2c5e2ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599262"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>Propriété canonique PidTagWizardNoPabPage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient TRUE si l’Assistant Profil doit supprimer la page du carnet d’adresses personnel.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Identificateur :  <br/> |0x6701  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Exchange Administrative  <br/> |
   
## <a name="remarks"></a>Remarques

Les fournisseurs de services peuvent définir cette propriété lors de l’appel d’une fonction basée sur le prototype de fonction [LAUNCHWIZARDENTRY.](launchwizardentry.md) Cette propriété indique à l’Assistant Profil que le fournisseur ne souhaite pas que la page du PAB s’affiche pendant la boîte de dialogue utilisateur. 
  
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

