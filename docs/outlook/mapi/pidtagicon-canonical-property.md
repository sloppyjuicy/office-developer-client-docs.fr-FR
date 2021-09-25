---
title: Propriété canonique PidTagIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 90ca5cef741f69d68f1db06098ca8133720a8130
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555348"
---
# <a name="pidtagicon-canonical-property"></a>Propriété canonique PidTagIcon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une image bitmap d’une icône pleine taille pour un formulaire. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ICON  <br/> |
|Identificateur :  <br/> |0x0FFD  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient une image de 32 × 32 pixels d’une icône, identique au contenu d’un . Fichier ICO. Cette propriété est normalement copiée à partir du . Fichier ICO spécifié dans la ligne LargeIcon de la section [Description] appropriée du fichier de configuration du formulaire. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMiniIcon](pidtagminiicon-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

