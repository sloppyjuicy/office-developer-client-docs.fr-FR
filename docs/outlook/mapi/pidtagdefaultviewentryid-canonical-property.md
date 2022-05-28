---
title: Propriété canonique PidTagDefaultViewEntryId
description: Décrit la propriété canonique PidTagDefaultViewEntryId, qui contient l’identificateur d’entrée de la vue par défaut d’un dossier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
ms.openlocfilehash: 45fd4080992835b31095374447f5d9bb8e826765
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769311"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Propriété canonique PidTagDefaultViewEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de la vue par défaut d’un dossier.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Identificateur :  <br/> |0x3616  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est l’identificateur d’entrée de l’affichage dossier qui doit être défini comme vue initiale. La propriété n’a pas besoin d’être définie si la vue « Normal » doit être utilisée comme vue initiale.
  
Une application cliente peut obtenir cette propriété au moment où elle ouvre le dossier et réaliser des gains de performances significatifs. Cette propriété peut être utilisée comme raccourci pour obtenir l’affichage par défaut, au lieu d’ouvrir la table des matières associée et d’envoyer une restriction.
  
Une implémentation de fournisseur de services de la méthode [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) peut copier cette propriété lorsqu’elle copie des dossiers. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
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

