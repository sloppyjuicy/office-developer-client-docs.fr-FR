---
title: Propriété canonique PidLidAddressBookProviderArrayType
description: La propriété canonique PidLidAddressBookProviderArrayType spécifie l’état des adresses électroniques du contact et représente un ensemble d’indicateurs de bits.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
ms.openlocfilehash: 7abfaa2e7eb55ea28d40000a243ecbcfe5d1b10f
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852952"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Propriété canonique PidLidAddressBookProviderArrayType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’état des adresses électroniques du contact et représente un ensemble d’indicateurs de bits.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidABPArrayType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008029  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la propriété **dispidABPArrayType** doit être une combinaison d’indicateurs qui spécifient l’état de l’objet contact. Les indicateurs individuels sont spécifiés dans le tableau suivant. Si cette propriété est définie, la propriété **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) doit également être définie. Ces deux propriétés doivent être synchronisées les unes avec les autres. Par exemple, si **dispidABPArrayType** a le bit « 0x00000001 défini », l’une des valeurs de **dispidABPEmailList** doit être « 0x00000000 ». 
  
|**Peu**|**Description**|
|:-----|:-----|
|0x00000001  <br/> |Email1 est défini pour le contact. |
|0x00000002  <br/> |Email2 est défini pour le contact. |
|0x00000004  <br/> |Email3 est défini pour le contact. |
|0x00000008  <br/> |La télécopie professionnelle est définie pour le contact. |
|0x00000010  <br/> |La télécopie d’accueil est définie pour le contact. |
|0x00000020  <br/> |La télécopie principale est définie pour le contact. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

