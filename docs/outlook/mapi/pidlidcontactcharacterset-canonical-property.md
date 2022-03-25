---
title: Propriété canonique PidLidContactCharacterSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: Spécifie le jeu de caractères utilisé pour ce contact. Les applications peuvent utiliser cette propriété pour faciliter la génération d’une liste de choix dépendant du jeu de caractères.
ms.openlocfilehash: fca6fc854cd95b49bd91b4a213980d08e0bed849
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406231"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a>Propriété canonique PidLidContactCharacterSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le jeu de caractères utilisé pour ce contact.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidContactCharSet  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008023  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Les applications peuvent utiliser cette propriété pour générer une liste de choix dépendant du jeu de caractères pour les propriétés **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) et **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)). Si la valeur de la propriété est « 0x00000000 » ou « 0x00000001 », les applications doivent traiter la propriété comme n’étant pas définie.
  
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

