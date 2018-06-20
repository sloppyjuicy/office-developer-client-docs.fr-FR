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
ms.openlocfilehash: d992c7ac43c736e01184e1f12b3ad366587c9b06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785644"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Propriété canonique PidTagAccessControlListTable

  
  
**S’applique à**: Outlook 
  
Contient un tableau qui se compose de tous les l’accès listes de contrôle système (SACL) appliqués à un dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ACL_TABLE  <br/> |
|Identificateur :  <br/> |0x3FE0  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Zone :  <br/> |Contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est présente sur tous les objets de dossier sur un serveur Exchange. Valeurs inclus dans cette propriété sont utilisées pour la lecture et de modification de contrôle d’accès les listes de dossiers. Vous pouvez utiliser la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’identificateur d’interface **IID_IExchangeModifyTable** pour obtenir un [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface à la table ACL sur un dossier. Vous pouvez utiliser cette interface pour lire et modifier les listes ACL. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

