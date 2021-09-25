---
title: Propriété canonique PidLidContactLinkSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c455687a44b0f35a237638eb0c951042a1346932
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583883"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>Propriété canonique PidLidContactLinkSearchKey

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la liste **de SearchKeys pour** le contact lié par cet objet de message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidContactLinkSearchKey  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008584  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

|**Longueur en octets**|**Description**|**Remarques**|
|:-----|:-----|:-----|
|2  <br/> |ContactEntryCount  <br/> |Aucun  <br/> |
|variable  <br/> |Données SearchKey  <br/> |Répète les heures ContactEntryCount  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi

- [Propriétés MAPI](mapi-properties.md) 
- [Propriétés canoniques MAPI](mapi-canonical-properties.md)
- [Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

