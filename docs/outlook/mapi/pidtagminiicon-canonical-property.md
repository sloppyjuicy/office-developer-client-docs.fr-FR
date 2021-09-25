---
title: Propriété canonique PidTagMiniIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96d477576f0d5fc8f94ec9e8d7e3f2fd3879aad1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595195"
---
# <a name="pidtagminiicon-canonical-property"></a>Propriété canonique PidTagMiniIcon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une image bitmap d’une icône à demi-taille pour un formulaire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MINI_ICON  <br/> |
|Identificateur :  <br/> |0x0FFC  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient une image de 32 × 32 pixels d’une icône, identique au contenu d’un . Le fichier ICO, mais seul le coin supérieur gauche de 16 × 16 pixels est considéré comme significatif. Cette propriété est normalement copiée à partir du . Fichier ICO spécifié dans la ligne SmallIcon de la section [Description] appropriée du fichier de configuration du formulaire.
  
 **Remarque** Certaines plateformes ne supportent pas les icônes de 16 × 16 pixels. Le format 32 × 32 de cette propriété est utilisable dans ce cas, mais les applications clientes doivent être sensibles aux incohérences d’affichage. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagIcon](pidtagicon-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

