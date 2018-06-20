---
title: Propriété canonique PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5d97f56946512266bb7a08aa6b4a4ff78dded56a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785114"
---
# <a name="pidlidcustomflag-canonical-property"></a>Propriété canonique PidLidCustomFlag

  
  
**S’applique à**: Outlook 
  
Masque de bits qui spécifie la façon dont un message personnalisé, par exemple, enregistré avec des propriétés personnalisées.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCustomFlag  <br/> |
|ID de type long (capot) :  <br/> |0x00008251  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, tout d’abord utiliser **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans **[IMAPIProp::GetProps](imapiprop-getprops.md)** pour obtenir la valeur. 
  
Indicateurs possibles sont les suivantes :
  
****

|**Constante**|**Valeur**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
Lors de l’appel **IMAPIProp::GetIDsFromNames**, spécifiez les valeurs suivantes pour la structure **[MAPINAMEID](mapinameid.md)** désignés par le paramètre d’entrée *lppPropNames* . 
  
****

|**Membre**|**Valeur**|
|:-----|:-----|
|lpGuid :  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_ID  <br/> |
|Kind.lID :  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

