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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348481"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Propriété canonique PidLidAddressBookProviderEmailList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique quelles propriétés d'adresse électronique sont définies sur le contact. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidABPEmailList  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Address  <br/> |
|ID long (couvercle):  <br/> |0x00008028  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Chaque valeur PT_LONG de cette propriété doit être unique dans la propriété et doit être définie sur l'une des valeurs indiquées dans le tableau suivant. Si cette propriété est définie, la propriété **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) doit également être définie. Ces deux propriétés doivent être synchronisées les unes avec les autres. Par exemple, si l'une des valeurs de **dispidABPEmailList** est «0x00000000», **dispidABPArrayType** doit avoir le bit «0x00000001» défini. 
  
|**Value**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |Email1 est défini pour le contact.  <br/> |
|0x00000001  <br/> |Email2 est défini pour le contact.  <br/> |
|0x00000002  <br/> |Email3 est défini pour le contact.  <br/> |
|0x00000003  <br/> |Business Fax est défini pour le contact.  <br/> |
|0x00000004  <br/> |Home Fax est défini pour le contact.  <br/> |
|0x00000005  <br/> |La télécopie principale est définie pour le contact.  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

