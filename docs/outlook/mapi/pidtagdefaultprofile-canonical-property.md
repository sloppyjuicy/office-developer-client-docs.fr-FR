---
title: Propriété canonique PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 032d260b42a47ce8fc65720f3b0b82695f6c3e0d
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454865"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Propriété canonique PidTagDefaultProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un profil utilisateur de messagerie est le profil MAPI par défaut.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Identificateur :  <br/> |0x3D04  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’apparaît pas en tant que propriété d’un objet, mais uniquement en tant que colonne dans une table de profils. Une application cliente peut utiliser [la méthode IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) pour désigner le profil par défaut. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

