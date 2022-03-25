---
title: Propriété canonique PidLidEmail2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: Spécifie le deuxième nom complet qui correspond à l’adresse de messagerie spécifiée pour le contact.
ms.openlocfilehash: 390d66294fbd14467f95d4eaa1de0b0ede1b011f
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781641"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a>Propriété canonique PidLidEmail2OriginalDisplayName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le deuxième nom complet qui correspond à l’adresse de messagerie spécifiée pour le contact.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidEmail2OriginalDisplayName  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008094  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Si la valeur de la propriété **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) est « SMTP », la valeur de la propriété **PidLidEmail2OriginalDisplayName** respective doit être égale à la valeur de la propriété **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) respective. L’objectif de cette propriété est d’afficher une adresse conviviale de remplacement équivalente à celle de **dispidEmail2EmailAddress**.
  
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

