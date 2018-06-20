---
title: Propriété canonique PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0db245efdd8aad73b0c094c35079f50925ca4478
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785915"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Propriété canonique PidTagDefaultViewEntryId

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’entrée de l’affichage de par défaut d’un dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Identificateur :  <br/> |0x3616  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est l’identificateur d’entrée de l’affichage du dossier qui doit être défini en tant que la vue initiale. La propriété ne doit pas être définie si l’affichage de « Normal » est utilisée en tant que la vue initiale.
  
Une application cliente peut obtenir cette propriété au moment où qu'il ouvre le dossier et réaliser des gains de performances. Cette propriété peut être utilisée comme un raccourci pour obtenir la vue par défaut, au lieu d’ouvrir la table de contenu associé et lui en envoyer une restriction.
  
Implémentation d’un fournisseur de services de la méthode [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) peut copier cette propriété lors de la copie des dossiers. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
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

