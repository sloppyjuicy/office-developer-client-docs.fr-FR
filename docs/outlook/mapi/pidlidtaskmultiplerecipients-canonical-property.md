---
title: Propriété canonique PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: Fournit des conseils d’optimisation sur les destinataires d’une tâche pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: b3e45aef4169ee8b774fa7630397f4afa546d6b5
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405418"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>Propriété canonique PidLidTaskMultipleRecipients

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des conseils d’optimisation sur les destinataires d’une tâche.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskMultRecips  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008120  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Si elle est définie, cette propriété doit être définie sur une opération **OR** au niveau du bit de zéro ou de plusieurs des valeurs suivantes. 
  
|**Name**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|Sent  <br/> |0x00000001  <br/> |La tâche a plusieurs destinataires principaux. |
|Received  <br/> |0x00000002  <br/> |Bien que l’indication Envoyée ne soit pas présente, le client a détecté que la tâche a plusieurs destinataires principaux. |
|Reserved  <br/> |0x00000004  <br/> |Cette valeur est réservée. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

