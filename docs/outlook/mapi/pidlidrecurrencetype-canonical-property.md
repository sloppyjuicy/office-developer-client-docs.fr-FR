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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9fecd67c370333064fd593634ad2a924a3005d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785348"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>Propriété canonique PidLidRecurrenceType

  
  
**S’applique à**: Outlook 
  
Spécifie le type de périodicité de la série périodique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidRecurType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008231  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie le type de périodicité de la série périodique en utilisant l’une des valeurs répertoriées ci-dessous.
  
|**Status**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |Un rendez-vous unique.  <br/> |
|rectypeDaily  <br/> |1  <br/> |Une périodicité quotidienne.  <br/> |
|rectypeWeekly  <br/> |2  <br/> |Une périodicité hebdomadaire.  <br/> |
|rectypeMonthly  <br/> |3  <br/> |Une périodicité mensuelle.  <br/> |
|rectypeYearly  <br/> |4  <br/> |Une périodicité annuelle.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

