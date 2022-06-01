---
title: Propriété canonique PidLidRecurrenceType
description: Décrit la propriété canonique PidLidRecurrenceType, qui spécifie le type de périodicité de la série périodique.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
ms.openlocfilehash: f5346679dd3112b348323ab8ff7462d5a19e7d4c
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817430"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>Propriété canonique PidLidRecurrenceType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le type de périodicité de la série périodique.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidRecurType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008231  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie le type de périodicité de la série périodique à l’aide de l’une des valeurs répertoriées ci-dessous.
  
|**État**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |Un rendez-vous d’instance unique. |
|rectypeDaily  <br/> |1  <br/> |Périodicité quotidienne. |
|rectypeWeekly  <br/> |2  <br/> |Modèle de périodicité hebdomadaire. |
|rectypeMonthly  <br/> |3  <br/> |Modèle de périodicité mensuelle. |
|rectypeYearly  <br/> |4  <br/> |Périodicité annuelle. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

