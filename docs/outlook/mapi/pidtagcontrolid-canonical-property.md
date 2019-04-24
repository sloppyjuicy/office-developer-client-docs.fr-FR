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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334740"
---
# <a name="pidtagcontrolid-canonical-property"></a>Propriété canonique PidTagControlId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur unique pour un contrôle utilisé dans une boîte de dialogue. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_ID  <br/> |
|Identificateur :  <br/> |0x3F07  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Table d'affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient un identificateur unique pour le contrôle. Cet identificateur doit contenir une structure de [GUID](guid.md) et une valeur binaire de type **long**. Tous les contrôles de la boîte de dialogue doivent utiliser le même **GUID** pour identifier le fournisseur de services, et chaque contrôle doit utiliser une valeur de **type long** unique pour s'assurer que les contrôles ne sont pas en conflit. 
  
Cette propriété est utilisée dans les notifications. Par exemple, les notifications envoyées sur la table d'affichage doivent définir cette propriété pour identifier de manière unique le contrôle à mettre à jour. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

