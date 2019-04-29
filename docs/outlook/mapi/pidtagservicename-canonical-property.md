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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438959"
---
# <a name="pidtagservicename-canonical-property"></a>Propriété canonique PidTagServiceName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom d'un service de messagerie tel que défini par l'utilisateur dans le fichier MapiSvc. inf.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Identificateur :  <br/> |0x3D09  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le nom contenu dans ces propriétés est propre au service de messagerie. Elle provient de la section [services] du fichier MapiSvc. inf.
  
Ces propriétés apparaissent sous la forme d'une colonne dans le tableau service de messagerie et peuvent être utilisées pour filtrer les services. Étant donné qu'il est utilisé pour identifier et filtrer des services, la valeur ne doit pas être localisée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

