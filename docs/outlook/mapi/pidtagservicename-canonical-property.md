---
title: Propriété canonique PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: Contient le nom d’un service de message tel que définie par l’utilisateur dans le fichier MapiSvc.inf. Le nom contenu dans ces propriétés est spécifique au service de message.
ms.openlocfilehash: d6a6bfe13ebfd481b61473ca083bd241bb61b82b
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456020"
---
# <a name="pidtagservicename-canonical-property"></a>Propriété canonique PidTagServiceName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom d’un service de message tel que définie par l’utilisateur dans le fichier MapiSvc.inf.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Identificateur :  <br/> |0x3D09  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le nom contenu dans ces propriétés est spécifique au service de message. Il provient de la section [Services] dans MapiSvc.inf.
  
Ces propriétés apparaissent en tant que colonnes dans la table des services de message et peuvent être utilisées pour filtrer les services. Étant donné qu’elle est utilisée pour identifier et filtrer les services, la valeur ne doit pas être localisée.
  
## <a name="related-resources"></a>Ressources connexes

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

