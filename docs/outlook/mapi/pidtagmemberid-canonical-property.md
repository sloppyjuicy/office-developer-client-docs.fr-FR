---
title: Propriété canonique PidTagMemberId
description: Décrit la propriété canonique PidTagMemberId, qui contient l’identificateur d’un membre de table qui a décrit les droits.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
ms.openlocfilehash: 62915d76ebcb2ad7751e8567d43c9c97170c2cbd
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752735"
---
# <a name="pidtagmemberid-canonical-property"></a>Propriété canonique PidTagMemberId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’un membre de table qui dispose des droits décrits sur un dossier ou une boîte aux lettres Microsoft Exchange Server.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MEMBER_ID  <br/> |
|Identificateur :  <br/> |0x6671  <br/> |
|Type de données :  <br/> |PT_I8  <br/> |
|Domaine :  <br/> |Contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété renvoie un identificateur unique à la table. Un identificateur d’utilisateur d’annuaire est associé à chaque identificateur de membre et est donné par cette propriété. Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour récupérer l’identificateur d’entrée de répertoire d’un membre disposant de droits explicites sur un dossier. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Gère la récupération des listes d’autorisations de dossiers stockées sur le serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

