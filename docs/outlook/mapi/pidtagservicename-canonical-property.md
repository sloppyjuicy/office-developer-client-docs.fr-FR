---
title: Propriété canonique PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 260a35af11b76b1867c693723c1a7fa8133082fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786782"
---
# <a name="pidtagservicename-canonical-property"></a>Propriété canonique PidTagServiceName

  
  
**S’applique à**: Outlook 
  
Contient le nom d’un service de message tel que défini par l’utilisateur dans le fichier MapiSvc.inf.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Identificateur :  <br/> |0x3D09  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le nom figurant dans ces propriétés est spécifique au service de message. Il s’agit de la section [Services] dans MapiSvc.inf.
  
Ces propriétés apparaissent sous la forme d’une colonne dans la table de service de message et peuvent être utilisées pour filtrer les services. Car elle est utilisée pour identifier et filtrer les services, la valeur ne doit pas être localisée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

