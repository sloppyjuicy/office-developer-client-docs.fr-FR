---
title: Propriété canonique PidLidEmail1OriginalDisplayName
description: Décrit la propriété canonique PidLidEmail1OriginalDisplayName, qui spécifie le premier nom d’affichage qui correspond à l’adresse e-mail d’un contact.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
ms.openlocfilehash: af614407fc8dfc0f2fae0de8dd35dc1f0be4a8df
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853500"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a>Propriété canonique PidLidEmail1OriginalDisplayName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le premier nom d’affichage qui correspond à l’adresse e-mail spécifiée pour le contact.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidEmail1OriginalDisplayName  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008084  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Si la valeur de la propriété **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) est « SMTP », la valeur de la propriété **dispidEmail1OriginalDisplayName** respective doit être égale à la valeur de la propriété **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) respective. Cette propriété affiche une autre adresse conviviale qui équivaut à celle de la propriété **dispidEmail1EmailAddress** . 
  
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

