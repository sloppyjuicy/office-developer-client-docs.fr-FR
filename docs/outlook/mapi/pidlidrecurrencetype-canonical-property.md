---
title: Propriété canonique PidLidRecurrenceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7a0ea0dfe236341815fe94fb570908d7034fc83e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315910"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>Propriété canonique PidLidRecurrenceType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le type de récurrence de la série périodique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidRecurType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008231  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie le type de récurrence de la série périodique à l’aide de l’une des valeurs répertoriées ci-dessous.
  
|**État**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |Rendez-vous d’instance unique.  <br/> |
|rectypeDaily  <br/> |1   <br/> |Une récurrence quotidienne.  <br/> |
|rectypeWeekly  <br/> |2   <br/> |Une récurrence hebdomadaire.  <br/> |
|rectypeMonthly  <br/> |3   <br/> |Une récurrence mensuelle.  <br/> |
|rectypeYearly  <br/> |4   <br/> |Une récurrence annuel.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

