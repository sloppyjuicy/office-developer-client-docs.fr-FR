---
title: Propriété canonique PidTagAccessControlListTable
description: Décrit la propriété canonique PidTagAccessControlListTable, qui contient une table qui se compose de toutes les sacls appliquées à un dossier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
ms.openlocfilehash: 0353dd687802ee4d77da54956170331c07e1ddbf
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817171"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Propriété canonique PidTagAccessControlListTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une table qui se compose de toutes les listes de contrôle d’accès système (SACL) appliquées à un dossier.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ACL_TABLE  <br/> |
|Identificateur :  <br/> |0x3FE0  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est présente sur tous les objets de dossier d’un Exchange Server. Les valeurs incluses dans cette propriété sont utilisées pour lire et modifier des listes de contrôle d’accès (ACL) sur des dossiers. Vous pouvez utiliser la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’identificateur **d’interface IID_IExchangeModifyTable** pour obtenir une interface [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) dans la table ACL d’un dossier. Vous pouvez utiliser cette interface pour lire et modifier ces listes de contrôle d’accès. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

