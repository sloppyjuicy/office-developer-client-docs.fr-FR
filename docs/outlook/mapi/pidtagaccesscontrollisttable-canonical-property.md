---
title: Propriété canonique PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332003"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Propriété canonique PidTagAccessControlListTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau qui se compose de toutes les listes de contrôle d'accès système appliquées à un dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ACL_TABLE  <br/> |
|Identificateur :  <br/> |0x3FE0  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Contrôle d'accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est présente sur tous les objets Folder sur un serveur Exchange. Les valeurs comprises dans cette propriété sont utilisées pour la lecture et la modification de listes de contrôle d'accès (ACL) sur les dossiers. Vous pouvez utiliser la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) avec l'identificateur d'interface **IID_IExchangeModifyTable** pour obtenir une interface [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) dans la table ACL d'un dossier. Vous pouvez utiliser cette interface pour lire et modifier ces listes de Contrã'le d'accès. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

