---
title: Propriété canonique PidLidAutoFillLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAutoFillLocation
api_type:
- COM
ms.assetid: e4db6cae-4730-45d0-8b8a-9bd484c8bd3f
description: Indique que la valeur de la propriété dispidLocation est définie sur la propriété PR_DISPLAY_NAME du RecipientRow qui représente une ressource.
ms.openlocfilehash: ddfa212af68a5d72b9d3a8ce224041f1c2250273
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781222"
---
# <a name="pidlidautofilllocation-canonical-property"></a>Propriété canonique PidLidAutoFillLocation

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique que la valeur de la propriété **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) est définie sur la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du RecipientRow qui représente une ressource.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidAutoFillLocation  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x0000823A  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

Pour plus d’informations sur RecipientRow, voir le protocole Message et Attachment Object comme spécifié dans [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).
  
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

