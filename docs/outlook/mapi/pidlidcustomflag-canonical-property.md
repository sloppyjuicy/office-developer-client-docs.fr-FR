---
title: Propriété canonique PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3e2f25cba725c5ce47ba62e9ea9ca69475c56122
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595517"
---
# <a name="pidlidcustomflag-canonical-property"></a>Propriété canonique PidLidCustomFlag

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Masque de bits qui spécifie la façon dont un message est personnalisé, par exemple, enregistré avec des propriétés personnalisées.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCustomFlag  <br/> |
|ID long (LID) :  <br/> |0x00008251  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, utilisez d’abord **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans **[IMAPIProp::GetProps](imapiprop-getprops.md)** pour obtenir la valeur. 
  
Les indicateurs possibles sont les suivants :
  
****

|**Constante**|**Valeur**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
Lorsque vous appelez **IMAPIProp::GetIDsFromNames**, spécifiez les valeurs suivantes pour la structure **[MAPINAMEID](mapinameid.md)** pointée par le paramètre d’entrée  *lppPropNames*  . 
  
****

|**Membre**|**Valeur**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_ID  <br/> |
|Kind.lID :  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

