---
title: Propriété canonique PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 163a7e88bdb6f6c22a608af2b5a0af961f033779
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583506"
---
# <a name="pidtagcontrolid-canonical-property"></a>Propriété canonique PidTagControlId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur unique pour un contrôle utilisé dans une boîte de dialogue. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_ID  <br/> |
|Identificateur :  <br/> |0x3F07  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Tableau d’affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient un identificateur unique pour le contrôle. Cet identificateur doit contenir une structure [GUID](guid.md) et une valeur binaire de type **LONG**. Tous les contrôles de la boîte de dialogue doivent utiliser le même **GUID** pour identifier le fournisseur de services, et chaque contrôle doit utiliser une valeur **LONG** unique pour s’assurer que les contrôles ne sont pas en conflit. 
  
Cette propriété est utilisée dans les notifications. Par exemple, les notifications envoyées sur le tableau d’affichage doivent définir cette propriété pour identifier de manière unique le contrôle à mettre à jour. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

