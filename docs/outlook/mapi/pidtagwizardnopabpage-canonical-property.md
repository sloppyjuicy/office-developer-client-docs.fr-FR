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
description: Cette propriété contient TRUE si l’Assistant Profil doit supprimer la page du carnet d’adresses personnel.
ms.openlocfilehash: b93a19c87b085396e3a25c98c9e0be47b1212de8
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455061"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>Propriété canonique PidTagWizardNoPabPage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient TRUE si l’Assistant Profil doit supprimer la page du carnet d’adresses personnel.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Identificateur :  <br/> |0x6701  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Exchange administrative  <br/> |
   
## <a name="remarks"></a>Remarques

Les fournisseurs de services peuvent définir cette propriété lors de l’appel d’une fonction basée sur le prototype de fonction [LAUNCHWIZARDENTRY](launchwizardentry.md) . Cette propriété indique à l’Assistant Profil que le fournisseur ne souhaite pas que la page du PAB s’affiche pendant la boîte de dialogue utilisateur. 
  
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

