---
title: Propriété canonique PidTagItemTemporaryflags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ec092e6cc6174e156dbfe7784143c9d74715eef7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392969"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a>Propriété canonique PidTagItemTemporaryflags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un indicateur qui indique qu’un message a été lu, mais ne pas marqué comme lus.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ITEM_TMPFLAGS  <br/> |
|Identificateur :  <br/> |0x1097  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans le dossier de recherche de Messages non lus d’Outlook pour suivre les messages qui ont été lus sans réellement les marquer comme lu, les supprimer à partir du dossier. Lorsque cette propriété est supprimée les modifications d’affichage et de l’élément est marqué comme étant en lecture. Cette propriété ne sera pas synchronisé sur le serveur Exchange.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

