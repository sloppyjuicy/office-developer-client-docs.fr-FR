---
title: Propriété canonique PidLidAppointmentColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7efffac9dd3a0b4060cd7c2735f2590712ac6868
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600707"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>Propriété canonique PidLidAppointmentColor

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la couleur à utiliser lors de l’affichage du calendrier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptColor  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008214  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie la couleur à utiliser lors de l’affichage du calendrier. Un client ou un serveur doit définir cette valeur pour la compatibilité ascendante avec les clients plus anciens. Il peut à la place afficher le calendrier en fonction de la valeur de la propriété **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) comme spécifié dans [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx). Lorsqu’elle est définie, la valeur doit être l’une des suivantes.
  
|**Valeur**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |Aucun  <br/> |
|0x00000001  <br/> |Rouge  <br/> |
|0x00000002  <br/> |Bleu  <br/> |
|0x00000003  <br/> |Vert  <br/> |
|0x00000004  <br/> |Gris  <br/> |
|0x00000005  <br/> |Orange  <br/> |
|0x00000006  <br/> |Cyan  <br/> |
|0x00000007  <br/> |Olive  <br/> |
|0x00000008  <br/> |Pourpre  <br/> |
|0x00000009  <br/> |Teal  <br/> |
|0x0000000A  <br/> |Jaune  <br/> |
   
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

