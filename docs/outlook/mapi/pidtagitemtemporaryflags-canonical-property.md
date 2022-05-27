---
title: Propriété canonique PidTagItemTemporaryflags
description: Décrit la propriété canonique PidTagItemTemporaryflags, qui contient un indicateur qui indique qu’un message a été lu, mais pas marqué comme lu.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
ms.openlocfilehash: d6dae99d539c804b57d24df5b4fff8f7cd64cca3
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752224"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a>Propriété canonique PidTagItemTemporaryflags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un indicateur qui indique qu’un message a été lu, mais pas marqué comme lu.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ITEM_TMPFLAGS  <br/> |
|Identificateur :  <br/> |0x1097  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans le dossier de recherche Messages non lus de Outlook pour effectuer le suivi des messages qui ont été lus sans les marquer comme lus, ce qui les supprimerait du dossier. Lorsque la vue change, cette propriété est supprimée et l’élément est marqué comme lu. Cette propriété ne sera pas synchronisée avec le Exchange Server.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

