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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384198"
---
# <a name="pidlidcustomflag-canonical-property"></a>Propriété canonique PidLidCustomFlag

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
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

