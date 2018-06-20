---
title: Propriété canonique PidTagMemberId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786231"
---
# <a name="pidtagmemberid-canonical-property"></a>Propriété canonique PidTagMemberId

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’un membre de la table qui possède les droits décrits dans une boîte aux lettres ou un dossier Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MEMBER_ID  <br/> |
|Identificateur :  <br/> |0x6671  <br/> |
|Type de données :  <br/> |PT_I8  <br/> |
|Zone :  <br/> |Contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété renvoie un identificateur unique pour le tableau. Un identificateur d’annuaire utilisateur est associé à l’identificateur de chaque membre et est fourni par cette propriété. Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour récupérer l’identificateur d’entrée de répertoire d’un membre disposant de droits explicites sur un dossier. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Gère la récupération des listes d’autorisations de dossier sont stockés sur le serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

