---
title: Propriété canonique PidTagControlId
description: Décrit la propriété canonique PidTagControlId, qui contient un identificateur unique pour un contrôle utilisé dans une boîte de dialogue.
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
ms.openlocfilehash: 58f2729d09c724e75ca0260c66ddd2558111449d
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770522"
---
# <a name="pidtagcontrolid-canonical-property"></a>Propriété canonique PidTagControlId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur unique pour un contrôle utilisé dans une boîte de dialogue. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_ID  <br/> |
|Identificateur :  <br/> |0x3F07  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Table d’affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient un identificateur unique pour le contrôle. Cet identificateur doit contenir une structure [GUID](guid.md) et une valeur binaire de type **LONG**. Tous les contrôles de la boîte de dialogue doivent utiliser le même **GUID** pour identifier le fournisseur de services, et chaque contrôle doit utiliser une valeur **LONG** unique pour s’assurer que les contrôles ne se heurtent pas. 
  
Cette propriété est utilisée dans les notifications. Par exemple, les notifications envoyées sur la table d’affichage doivent définir cette propriété pour identifier de manière unique le contrôle à mettre à jour. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

