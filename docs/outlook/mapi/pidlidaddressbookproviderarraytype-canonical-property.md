---
title: Propriété canonique PidLidAddressBookProviderArrayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3515d0f751cb6d8d0d427079691456519bac97dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784955"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Propriété canonique PidLidAddressBookProviderArrayType

  
  
**S’applique à**: Outlook 
  
Spécifie l’état de l’adresse électronique du contact et représente un ensemble d’indicateurs de bits.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidABPArrayType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x00008029  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la propriété **dispidABPArrayType** doit être une combinaison des indicateurs qui spécifient l’état de l’objet contact. Indicateurs individuels sont spécifiés dans le tableau suivant. Si cette propriété est définie, la propriété **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) doit être définie. Ces deux propriétés doivent être conservées synchronisées entre eux. Par exemple, si **dispidABPArrayType** a le bit « 0 x 00000001 set », une des valeurs de **dispidABPEmailList** doit être « 0 x 00000000 ». 
  
|**Bit**|**Description**|
|:-----|:-----|
|0x00000001  <br/> |E-mail1 est défini pour le contact.  <br/> |
|0x00000002  <br/> |2 est défini pour le contact.  <br/> |
|0 x 00000004  <br/> |Messagerie3 est défini pour le contact.  <br/> |
|0 x 00000008  <br/> |Télécopie (bureau) est définie pour le contact.  <br/> |
|0 x 00000010  <br/> |Télécopie (domicile) est définie pour le contact.  <br/> |
|0 x 00000020  <br/> |Télécopie principal est défini pour le contact.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

