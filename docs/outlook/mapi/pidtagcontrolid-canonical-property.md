---
title: Propriété canonique PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2868533e0383309e013bb82aaa4300a0a40e335a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577512"
---
# <a name="pidtagcontrolid-canonical-property"></a>Propriété canonique PidTagControlId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un identificateur unique pour un contrôle utilisé dans une boîte de dialogue. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_ID  <br/> |
|Identificateur :  <br/> |0x3F07  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Afficher une table MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient un identificateur unique pour le contrôle. Cet identificateur doit contenir une structure [GUID](guid.md) et une valeur de type **LONG**binary. Tous les contrôles dans la boîte de dialogue doivent utiliser le même **GUID** pour identifier le fournisseur de services, et chaque contrôle doit utiliser un unique valeur de **type LONG** pour s’assurer que les contrôles n’entrent pas en conflit. 
  
Cette propriété est utilisée dans les notifications. Par exemple, notifications envoyées sur le tableau de l’affichage doivent définir cette propriété pour identifier le contrôle à mettre à jour. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

