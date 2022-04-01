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
description: Contient une image bitmap d’une icône à demi-taille pour un formulaire. Seul le coin supérieur gauche de 16 × 16 pixels est considéré comme significatif.
ms.openlocfilehash: b1830c6fb3683236a8ebc7808467824f782f465d
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523750"
---
# <a name="pidtagminiicon-canonical-property"></a>Propriété canonique PidTagMiniIcon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une image bitmap d’une icône à demi-taille pour un formulaire.
  
|Propriété |Valeur |
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

