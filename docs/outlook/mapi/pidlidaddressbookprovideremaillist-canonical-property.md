---
title: Propriété canonique PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fc11c47170792e5fef2e87786ff564901f505022
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62789087"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Propriété canonique PidLidAddressBookProviderEmailList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les propriétés d’adresse électronique définies sur le contact. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidABPEmailList  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008028  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Chaque PT_LONG de cette propriété doit être unique dans la propriété et doit être définie sur l’une des valeurs du tableau suivant. Si cette propriété est définie, la propriété **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) doit également être définie. Ces deux propriétés doivent être synchronisées l’une avec l’autre. Par exemple, si l’une des valeurs dans **dispidABPEmailList** est « 0x00000000 », **dispidABPArrayType** doit avoir le bit « 0x00000001 » définie. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |Email1 est défini pour le contact. |
|0x00000001  <br/> |Email2 est défini pour le contact. |
|0x00000002  <br/> |Email3 est défini pour le contact. |
|0x00000003  <br/> |La télécopie professionnelle est définie pour le contact. |
|0x00000004  <br/> |La télécopie à domicile est définie pour le contact. |
|0x00000005  <br/> |La télécopie principale est définie pour le contact. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

