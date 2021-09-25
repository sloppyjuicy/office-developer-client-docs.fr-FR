---
title: Propriété canonique PidTagItemTemporaryflags
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7ff4506722befb72c6cc707adedc66fceb44f484
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587544"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a>Propriété canonique PidTagItemTemporaryflags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un indicateur qui indique qu’un message a été lu, mais pas marqué comme lu.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ITEM_TMPFLAGS  <br/> |
|Identificateur :  <br/> |0x1097  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans le dossier de recherche Messages non lus de Outlook pour effectuer le suivi des messages qui ont été lus sans les marquer comme lus, ce qui les supprimerait du dossier. Lorsque l’affichage change, cette propriété est supprimée et l’élément est marqué comme lu. Cette propriété ne sera pas synchronisée avec le Exchange Server.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

