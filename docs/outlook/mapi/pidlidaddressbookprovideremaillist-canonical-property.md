---
title: Propriété canonique PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9f73720860aa0ec54289f25a553bb00bfbe76b6a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581047"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Propriété canonique PidLidAddressBookProviderEmailList

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie les propriétés de l’adresse électronique du contact. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidABPEmailList  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x00008028  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Chaque valeur PT_LONG dans cette propriété doit être unique dans la propriété et doit être défini sur une des valeurs dans le tableau suivant. Si cette propriété est définie, la propriété **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) doit également être définie. Ces deux propriétés doivent être conservées synchronisées entre eux. Par exemple, si une des valeurs de **dispidABPEmailList** est « 0 x 00000000 », puis **dispidABPArrayType** doit avoir le bit « 0 x 00000001 » défini. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |E-mail1 est défini pour le contact.  <br/> |
|0x00000001  <br/> |2 est défini pour le contact.  <br/> |
|0x00000002  <br/> |Messagerie3 est défini pour le contact.  <br/> |
|0 x 00000003  <br/> |Télécopie (bureau) est définie pour le contact.  <br/> |
|0 x 00000004  <br/> |Télécopie (domicile) est définie pour le contact.  <br/> |
|0 x 00000005  <br/> |Télécopie principal est défini pour le contact.  <br/> |
   
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
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

