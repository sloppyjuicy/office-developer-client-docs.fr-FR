---
title: Propriété canonique PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6cd255c60987ec7a279e509aa2925a8029cce62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785895"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Propriété canonique PidTagDefaultProfile

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si un profil utilisateur de messagerie est le profil par défaut MAPI.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Identificateur :  <br/> |0x3D04  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’apparaît pas en tant que propriété de tout objet, mais uniquement en tant que colonne dans une table de profil. Une application cliente peut utiliser la méthode [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) pour désigner le profil par défaut. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

