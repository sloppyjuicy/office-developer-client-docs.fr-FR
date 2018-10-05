---
title: Propriété canonique PidTagViewDescriptorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ab906d83ae4ad46747fd9037728620db1d656d25
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394768"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a>Propriété canonique PidTagViewDescriptorName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom d’un descripteur d’affichage.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W  <br/> |
|Identificateur :  <br/> |0x7006  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message défini par la classe transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés doivent être définies sur une chaîne vide pour un message de dossier associer des informations (FAI) qui contient les définitions d’affichage.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.
    
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

