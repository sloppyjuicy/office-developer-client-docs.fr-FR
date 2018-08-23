---
title: Propriété canonique PidTagWizardNoPabPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cdb7dde4853188eb0621dc3c2f45c2dc713441d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570239"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>Propriété canonique PidTagWizardNoPabPage

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette propriété contient la valeur TRUE si l’Assistant profil consiste à supprimer de la page de carnet d’adresses personnel.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Identificateur :  <br/> |0x6701  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |D’administration Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Fournisseurs de services peuvent définir cette propriété lors de l’appel d’une fonction basée sur le prototype de la fonction [LAUNCHWIZARDENTRY](launchwizardentry.md) . Cette propriété indique à l’Assistant profil que le fournisseur ne souhaite pas la page de carnet d’adresses personnel s’affiche au cours de la boîte de dialogue utilisateur. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

